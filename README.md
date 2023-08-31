# serverless-struct-validation
This composite action will verify the structure of your repositrory if it's compatible with the structure of ttv-apis

## Obligatory structure
You should have a principal folder src that will have a subfolder named services in this folder you will add your specific service with the following syntaxe *-service this sfolder will contain all the necessary files of your app for example: handlers, serverless.yml etc

```
.
├── src
│   ├── services               # Lambda configuration and source code folder
│   │   ├── service
│   │      ├── handler.ts      # `service` lambda source code
│   │      ├── serverless.yml        # `Hello` lambda Serverless 

```
## Example usage

```yaml
- name: Validate structure
  uses: TrouveTaVoie/serverless-struct-validation@main