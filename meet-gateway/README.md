```
curl -H "host: store.example.com" 34.117.240.126

curl -s -H "host: store.example.com" 34.117.240.126 | grep 'metadata'

curl -s -H "host: store.example.com" 34.117.240.126/de | grep 'metadata'

curl -s -H "host: store.example.com" -H "env: canary " 34.117.240.126 | grep 'metadata'

while true; do curl -s -H "host: store.example.com" 34.117.240.126 | grep 'metadata'; done;

curl -s -H "host: site.example.com" 34.117.240.126 | grep 'metadata'