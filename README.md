# <img src=".gitlab/avatar.png" alt="avatar" height="20"/> prepare

[![](https://gitlab.com/pl.rachuna-net/cicd/components/prepare/-/badges/release.svg)](https://gitlab.com/pl.rachuna-net/cicd/components/prepare/-/releases)
[![](https://gitlab.com/pl.rachuna-net/cicd/components/prepare/badges/main/pipeline.svg)](https://gitlab.com/pl.rachuna-net/cicd/components/prepare/-/commits/main)

Komponent do przygotowania procesu CI/CD.

* [🔍 Input Parameters](docs/input_parameters.md)
* [🔍 Analyze Conventional Commits](docs/conventional_commits.md)

---
## 🧪 Przykład użycia

```yaml
include:
  - component: $CI_SERVER_FQDN/pl.rachuna-net/cicd/components/prepare/input_parameters@$COMPONENT_VERSION_PREPARE
    inputs:
      docker_image: $CONTAINER_IMAGE_PYTHON

  - component: $CI_SERVER_FQDN/pl.rachuna-net/cicd/components/prepare/conventional_commits@$COMPONENT_VERSION_PREPARE
    inputs:
      docker_image: $CONTAINER_IMAGE_PYTHON

🔍 input parameters:
  stage: prepare
  rules:
    - when: on_success

🔍 Analize Conventional Commits:
  stage: prepare
  rules:
    - when: on_success
```

---
## Contributions
Jeśli masz pomysły na ulepszenia, zgłoś problemy, rozwidl repozytorium lub utwórz Merge Request. Wszystkie wkłady są mile widziane!
[Contributions](CONTRIBUTING.md)

---
## License
Projekt licencjonowany jest na warunkach [Licencji MIT](LICENSE).

---
# Author Information
### &emsp; Maciej Rachuna
# <img src="https://gitlab.com/pl.rachuna-net/gitlab-profile/-/raw/main/assets/logo/website_logo_transparent_background.png" alt="rachuna-net.pl" height="100"/>
