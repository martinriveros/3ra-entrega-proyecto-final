# Ecommerce (3rd delivery)


## To run

Install all dependencies

```bash
npm install
npm i artillery -g
```
Then you have two scripts predefined (e.g: "npm run dev") to help you get the e commerce runnig:
```bash
npm run dev:      cross-env NODE_ENV=development nodemon index.js --portCLI 8080
```
```bash
npm run cluster:  node index.js --mode cluster --portCLI 8080

```
Each of the above need to be run before the corresponding:

```bash
artillery quick --count 50 -n 40 http://localhost:8080/index > result_fork.txt

```
```bash
artillery quick --count 50 - n 20 artillery quick --count 50 -n 40 http://localhost:8088/index > result_cluster.txt
```

## Entry point

```bash
localhost:8080/api/index
```
## Work in progress

Message sending trough [Whatsapp](https://www.whatsapp.com/?lang=es) is still not working due to restrictions to free account by [Twilio](https://www.twilio.com/es-mx/)

## Enjoy this next saturday night