## Kubernetes cwiczenia

1. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami. Wykonac testy usunięcia danych podów i zweryfikowac czas uruchomienia kolejnego poda.
2. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami + utworzyc obiekt Service rodzaju ClusterIP i wystawic na zewnatrz na porcie 88.
- dodatkowo utworzyc pod Ubuntu (alternatywnie - nginx) i doinstalowac curl i odpytac z wewnatrz poda adres nginx service ClusterIP
3. Przy uzyciu obiektu deployment uruchomic aplikację nginx i ustawic LivenessProbe - weryfikacja czy prawidłowo działa nginx.
4. Przy uzyciu obiektu deployment uruchomic DataBase Postgress - wystawic niezbedne porty + ustawic resources limits + ReadinessProbe
5. Zaimpelentowac definicję pod-failed.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
6. Zaimpelentowac definicję mysql-deploy.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
7. Uruchomic aplikacje ToDos na Kubernetes korzystajac z pomocy docker-compose.yaml. 
8. Uruchomic Wordpress + DB na Kubernetes 