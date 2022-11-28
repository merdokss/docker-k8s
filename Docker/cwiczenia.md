- Nginx z wystawieniem katalogu
- Wystawimy nginx z podmienioną zawartością katalogu "/usr/share/nginx/html" - wrzucic katalog "elements-www"
- Uruchomic kontener o nazwach - nginx-1 oraz nginx-2 na podstwawie obrazu nginx. Następnie wejsc do środka jednego z nich i odpytac drugiego na porcie 80. 
`curl http://nginx-2:80`
- Zbudowac obraz z wlasnym plikiem index.html (/usr/share/nginx/html/index.html). Następnie uruchomic kontener z obrazu i wystawic port 80 na host-a. 