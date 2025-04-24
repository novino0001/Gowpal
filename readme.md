## All Chalk Backend

### Setup

`npm install` or `npm ci`

### Local DB Setup

1. Install Docker Desktop if not installed already
2. Run `docker compose up -d` command to pull the PostgreSQL image and run the container
3. Turn on synchronization in the Database configuration

### Run Server

1. Local Environment: `npm start`
2. Testing Environment: `npm run dev`
3. Staging Environment: `npm run staging`

### Custom Library Integration

- The commonly used entities, types, methods and properties are accessible from the `common-lib` library which is fetched directly from the repository url
- The value after `#` (5e4ab0a533f7ba54695b6c479a8c94c19783ce0a) is the commit sha of `https://git-codecommit.us-east-1.amazonaws.com/v1/repos/all-chalk-backend-lib` repository, you can replace this if you make any change in the common library code

```json
{
	"dependencies": {
		"@aws-sdk/client-secrets-manager": "^3.600.0",
		"@sendgrid/mail": "^8.1.3",
		"@sentry/node": "^8.9.2",
		"aws-serverless-express": "^3.4.0",
		"bcryptjs": "^2.4.3",
		"cookie-parser": "^1.4.6",
		"cors": "^2.8.5",
		"crypto-js": "^4.2.0",
		"ejs": "^3.1.10",
		"express": "^4.18.2",
		"firebase-admin": "^12.3.0",
		"joi": "^17.13.1",
		"jsonwebtoken": "^9.0.2",
		"pg": "^8.12.0",
		"reflect-metadata": "^0.2.2",
		"swagger-jsdoc": "^6.2.8",
		"swagger-ui-express": "^5.0.1",
		"typeorm": "^0.3.20",
		"common-lib": "git+https://git-codecommit.us-east-1.amazonaws.com/v1/repos/all-chalk-backend-lib#5e4ab0a533f7ba54695b6c479a8c94c19783ce0a"
	}
}
```
