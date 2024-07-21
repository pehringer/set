# ***map***
Are you looking for a versatile associative array for C? Look no further. This library offers a hash table that utilizes Robin Hood hashing, a technique that dynamically rearranges keys to keep them close to their ideal hash locations, resulting in a fast and reliable associative array.
- Easy to use (library only has eight functions)
  + [```Map* map_Init(const size_t key, const size_t val, const size_t cap)```](#map-map_initconst-size_t-key-const-size_t-val-const-size_t-cap)
  + [```void map_Free(Map *m)```](#void-map_freemap-m)
  + [```size_t map_Cap(Map *m)```](#size_t-map_capmap-m)
  + [```size_t map_Len(Map *m)```](#size_t-map_lenmap-m)
  + [```void map_Del(Map *m, const void *key)```](#void-map_delmap-m-const-void-key)
  + [```void* map_Set(Map *m, const void *key)```](#void-map_setmap-m-const-void-key)
  + [```const void* map_Get(Map *m, const void *key)```](#const-void-map_getmap-m-const-void-key)
  + [```const void* map_Iter(Map *m, const void *key)```](#const-void-map_itermap-m-const-void-key)
- Generic (keys and values can be any kind of data)
- Lightweight (less than XXX lines of source code)
- Performant (Robin Hood hashing dynamically rearranges keys)
- Portable (only uses the C standard library)
  + ```stdlib.h```
  + ```string.h```
# Example Code
# Library Functions
---
### ```Map* map_Init(const size_t key, const size_t val, const size_t cap)```
Allocates map with specified key-value sizes and capacity.
- ```key``` size of key type.
- ```val``` size of value type.
- ```cap``` capacity of map.
---
### ```void map_Free(Map *m)```
Deallocates map.  
- ```m``` map returned by map_Init.
---
### ```size_t map_Cap(Map *m)```
Returns the total number of key-value pairs.  
- ```m``` map returned by map_Init.
---
### ```size_t map_Len(Map *m)```
Returns the current number of key-value pairs being used.  
- ```m``` map returned by map_Init.
---
### ```void map_Del(Map *m, const void *key)```
Removes the key and its value if the key is present.  
- ```m``` map returned by map_Init.
- ```key``` key to delete.
---
### ```void* map_Set(Map *m, const void *key)```
Inserts the key with a zero value if the key is not present.  
Returns NULL if the insert fails (map is full).  
Otherwise, returns a pointer to the key's value.  
- ```m``` map returned by map_Init.
- - ```key``` key to update or insert.
---
### ```const void* map_Get(Map *m, const void *key)```
Returns a pointer to the key’s value if the key is present.  
Otherwise, returns NULL (not in map).  
- ```m``` map returned by map_Init.
- ```key``` key to lookup.
---
### ```const void* map_Iter(Map *m, const void *key)```
Returns a pointer to the first key if the key is NULL.  
Returns NULL if the key was the last key or not present.  
Otherwise, returns a pointer to the next key.  
- ```m``` map returned by map_Init.
- ```key``` current key iteration.
---
