# 🛠 Job template: Input Parameters

Job, który wyświetla informacje o zmiennych procesowych CI

## ⚙️ Parametry wejściowe (`inputs`)

| Nazwa          | Typ    | Domyślna wartość                                             | Opis                                              |
| -------------- | ------ | ------------------------------------------------------------ | ------------------------------------------------- |
| `docker_image` | string | `registry.gitlab.com/pl.rachuna-net/containers/python:2.0.1` | Obraz Dockera z interpreterem Pythona lub shellem |

---
## 🧬 Zmienne środowiskowe obsługiwane przez skrypt

Komponent wypisuje wartości m.in. następujących zmiennych:

* `GITLAB_CI_VERSION`
* `COMPONENT_VERSION_*`
* `COMPONENT_VERSION_DEPLOY`
* `CONTAINER_IMAGE_*`
* `CONTAINER_IMAGE_PYTHON`
* `VAULT_ADDR`
* `SONAR_HOST_URL`

---
## 📤 Output

Skrypt wypisuje dane w formie tabeli ASCII w logach pipeline’u, np.:

```
===> 💾 Print set inputs Variables
┌────────────────────────────────┬──────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ Variable                       │ Value                                                                                                │
├────────────────────────────────┼──────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ CONTAINER_IMAGE_PYTHON         │ registry.gitlab.com/pl.rachuna-net/containers/python:2.0.1                                           │
│ COMPONENT_VERSION_DEPLOY       │ v1.2.3                                                                                               │
...
└────────────────────────────────┴──────────────────────────────────────────────────────────────────────────────────────────────────────┘
```
