### m3u8
---
https://github.com/globocom/m3u8

```py
import m3u8

m3u8_obj = m3u8.load('http://videoserver.com/playlist.m3u8')
print m3u8_obj.segments
print m3u8_obj.target_duration

m3u8_obj = m3u8.loads('#EXTM3U8 ... etc ...')

import m3u8

m3u8_obj = m3u8.loads('#EXTM3U8 ... etc ...')
len(m3u8_obj.keys)
for key in m3u8_obj.keys:
  if key:
    key.uri
    key.method
    key.iv
    

import m3u8

m3u8_obj = m3u8.loads('#EXTM3U8 ... etc ...')
segmk1 = m3u8_obj.segmetns.by_key(None)

segm = m3u8_obj.segments.by_key( m3u8_obj.keys[-1] )

import m3u8

m3u8_obj = m3u8.loads('#EXTM3U8 ... etc ..')

new_key = m3u8.Key("AES-128", "/encrypted/newkey.bin", None, iv = "xxx")
for segment in m3u8_obj.segments.by_key( m3u8_obj.keys[-1] ):
  segm.key = new_key
m3u8_obj.keys[-1] = new key

variant_m3u8 = m3u8.loads('EXTM3U8 ... contains a variant stream ...')
variant_m3u8.is_variant

for playlist in variant_m3u8.playlists:
  playlist.uri
  playlist.stream_info.bandwidth
  

variant_m3u8 = m3u8.loads('#EXTM3U ... contains a variant stream ...')
for iframe_playlist in variant_m3u8.iframe_playlists:
  iframe_playlist.uri
  iframe_playlist.iframe_stream_info.bandwidth
  
import m3u8

def get_movie(line, data, lineno):
  if line.startswith('#MOVIE-NAME'):
    custom_tag = line.split(':')
    data['movie'] = custom_tag[1].strip()
    
meu8_obj = m3u8.load('http://videoserver.com/playlist.m3u8', custom_tags_parser=get_movie)
print(m3u8_obj.data['movie'])
```

```sh
./runtests
```

```
```


