## Kubernetes cwiczenia

1. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami. Wykonac testy usunięcia danych podów i zweryfikowac czas uruchomienia kolejnego poda.
2. Utworzyc ReplicaSet dla aplikacji nginx z ustawionymi 4 replikami + utworzyc obiekt Service rodzaju LoadBalancer i wystawic na zewnatrz na porcie 8888.
3. Przy uzyciu obiektu deployment uruchomic aplikację nginx i ustawic LivenessProbe - weryfikacja czy prawidłowo działa nginx.
4. Przy uzyciu obiektu deployment uruchomic DataBase Postgress - wystawic niezbedne porty + ustawic resources limits + ReadinessProbe
5. Zaimpelentowac definicję pod-failed.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
6. Zaimpelentowac definicję pod-failed.yaml i zweryfikowac poprawnosc uruchomienia zasobow. W razie potrzeby poprawic konfiguracje
7. Uruchomic aplikacje ToDos na Kubernetes korzystajac z pomocy docker-compose.yaml. 