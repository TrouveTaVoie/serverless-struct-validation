# Serverless Structure Validation

This composite action will verify the structure of your repositrory if it's compatible with the structure of ttv-apis.

## General structure

```
├── src
│   ├── services               # Lambda configuration and source code folder
│   │   ├── <service-name>-service
│   │      ├── handler.ts      # `service` lambda source code
│   │      ├── serverless.yml        # `Hello` lambda Serverless
│   │      ├── README.md      # the readme that explain your app
│   └── resources     # ressources used by multiple services
│       └── <service-name>-resources.yml    # aws resources of each service
```

## Mandatory structure

You should have a main folder `src` that will have a subfolder named `services` in this folder you will add your specific service with the following syntaxe \*-service this folder will contain all the necessary files of your app for example: handlers, `serverless.yml`, etc.

```
.
├── src
│   ├── services               # Lambda configuration and source code folder
│   │   ├── <service-name>-service
│   │      ├── handler.ts      # `service` lambda source code
│   │      ├── serverless.yml        # `Hello` lambda Serverless

```

## Optional strucuture

If your service have a resources that should be deployed in the cloud provider you can add it into (`src/resources`) create a yaml file there specify the name as mentioned before `<service-name>-resources.yml` and don't forget to put the path in your `serverless.yml` to deploy structure

```
├── src
│   ├── services               # Lambda configuration and source code folder
│   └── resources     # ressources used by multiple services
│       └── <service-name>-resources.yml    # aws resources of each service
```

## Example usage

```yaml
- name: Validate structure
  uses: TrouveTaVoie/serverless-struct-validation@main
```
