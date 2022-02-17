# RPM# Use la última versión 2.1 del motor de proceso de tubería CircleCI.
# Ver: https://circleci.com/docs/2.0/configuration-reference
versión : 2.1

# Defina un trabajo para invocarlo más tarde en un flujo de trabajo.
# Ver: https://circleci.com/docs/2.0/configuration-reference/#jobs
trabajos :
  decir-hola :
    # Especifique el entorno de ejecución. Puede especificar una imagen de Dockerhub o usar una de nuestras Imágenes de conveniencia del Centro de desarrolladores de CircleCI.
    # Ver: https://circleci.com/docs/2.0/configuration-reference/#docker-machine-macos-windows-executor
    ventana acoplable :
      - imagen : cimg/base:estable
    # Agregar pasos al trabajo
    # Ver: https://circleci.com/docs/2.0/configuration-reference/#steps
    pasos :
      - pago
      - ejecutar :
          nombre : " Di hola "
          comando : " echo ¡Hola, mundo! "

# Invocar trabajos a través de flujos de trabajo
# Ver: https://circleci.com/docs/2.0/configuration-reference/#workflows
flujos de trabajo :
  decir-hola-flujo de trabajo :
    trabajos :
      - saludar 
# Generar recursos para la gente 
