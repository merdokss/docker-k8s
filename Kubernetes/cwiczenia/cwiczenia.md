## Kubernetes cwiczenia

### Pod, ReplicaSet
- Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami. Wykonac testy usunięcia danych podów i zweryfikowac czas uruchomienia kolejnego poda.
- Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami + utworzyc obiekt Service rodzaju ClusterIP i wystawic na zewnatrz na porcie 88.
- Utworzyc dwa Pody z nginx z labels app=nginx oraz dwa pody z httpd z labels app=nginx. Dodatkowo utworzyc service LoadBalancer (label - app=nginx) i sprawdzic jak działa ruch sieciowy.
### Deployment, LivenessProbe, Resources 
- Przy uzyciu obiektu deployment uruchomic aplikację httpd i ustawic LivenessProbe - weryfikacja czy prawidłowo działa httpd.
- Przy uzyciu obiektu deployment uruchomic DataBase Postgress - wystawic niezbedne porty + ustawic resources limits + ReadinessProbe

### Troubleshooting
- Zaimpelentowac definicję pod-failed.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
- Zaimpelentowac definicję mysql-deploy.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje

### App + DB
- Uruchomic aplikację ToDoS na Kubernetes - stworzyc 2 deploymenty oraz postawic DB Mongo, dodatkowo dla kazdego z komponentow utworzyc obiekt Service w celu komunikacje sieciowej
- Uruchomic Wordpress + DB na Kubernetes 