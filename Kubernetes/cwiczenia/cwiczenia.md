## Kubernetes cwiczenia

### Pod, ReplicaSet
1. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami. Wykonac testy usunięcia danych podów i zweryfikowac czas uruchomienia kolejnego poda.
2. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami + utworzyc obiekt Service rodzaju ClusterIP i wystawic na zewnatrz na porcie 88.
### Deployment, LivenessProbe, Resources 
3. Przy uzyciu obiektu deployment uruchomic aplikację httpd i ustawic LivenessProbe - weryfikacja czy prawidłowo działa httpd.
4. Przy uzyciu obiektu deployment uruchomic DataBase Postgress - wystawic niezbedne porty + ustawic resources limits + ReadinessProbe

### Troubleshooting
5. Zaimpelentowac definicję pod-failed.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
6. Zaimpelentowac definicję mysql-deploy.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje

### App + DB
7. Uruchomic aplikację ToDoS na Kubernetes - stworzyc 2 deploymenty oraz postawic DB Mongo, dodatkowo dla kazdego z komponentow utworzyc obiekt Service w celu komunikacje sieciowej
8. Uruchomic Wordpress + DB na Kubernetes 