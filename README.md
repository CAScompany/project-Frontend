# project-Frontend
Flujos de trabajo de GitHub Actions para Frontend

Introducción
Este repositorio contiene tres flujos de trabajo de GitHub Actions diseñados para facilitar la implementación de Frontend en diferentes entornos: DEV, PROD y STAGE. Cada flujo de trabajo está definido en un archivo YAML separado: workflow-dev.yml, workflow-prod.yml y workflow-stage.yml. A continuación, una descripción general de la estructura y el contenido de cada flujo de trabajo.

workflow-dev.yml
Propósito:
Este flujo de trabajo se activa en push al branch dev, eventos de despacho de repositorio de tipo build-dev y desencadenadores manuales de flujo de trabajo.

Concurrencia
Aplica control de concurrencia según el entorno de GitHub, permitiendo solo una ejecución del flujo de trabajo por entorno para evitar conflictos.

Trabajos
build-dev
Utiliza el flujo de trabajo de implementación definido en CAScompany/project-Frontend/.github/workflows/deploy-to-s3.yml en el branch dev.
Configura variables específicas del entorno para CI, Contentful, AWS, SonarQube y Slack.
workflow-prod.yml
Propósito
Se activa en envíos al branch main, eventos de despacho de repositorio de tipo build-prod y desencadenadores manuales de flujo de trabajo.

Concurrencia
Aplica control de concurrencia según el entorno de GitHub, permitiendo solo una ejecución del flujo de trabajo por entorno para evitar conflictos.

Trabajos
build-prod
Utiliza el flujo de trabajo de implementación definido en CAScompany/project-Frontend/.github/workflows/deploy-to-s3.yml en el branch main.
Configura variables específicas del entorno para CI, Contentful, AWS, SonarQube y Slack.
workflow-stage.yml
Propósito
Se activa en envíos al branch test, eventos de despacho de repositorio de tipo build-staging y desencadenadores manuales de flujo de trabajo.

Concurrencia
Aplica control de concurrencia según el entorno de GitHub, permitiendo solo una ejecución del flujo de trabajo por entorno para evitar conflictos.

Trabajos
build-staging
Utiliza el flujo de trabajo de implementación definido en CAScompany/project-Frontend/.github/workflows/deploy-to-s3.yml en el branch test.
Configura variables específicas del entorno para CI, Contentful, AWS, SonarQube y Slack.