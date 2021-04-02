# React Enviroment Setup using `env-cmd`

## install `env-cmd` using following command.

### `npm install env-cmd or npm install -g env-cmd`

## After instaling `env-cmd` create one file in root `.env-cmdrc`

inside `.env-cmdrc` file put json `env` data

```
{
    "dev":{
        "REACT_APP_BASE_URL": "development"
    },
    "staging":{
        "REACT_APP_BASE_URL": "staging"
    },
    "prod":{
        "REACT_APP_BASE_URL": "production"
    }

}
```

## Use `.env-cmdrc` file var in `package.json` file.

```
"scripts": {
    "dev": "env-cmd -e dev react-scripts start",
    "build-dev": "env-cmd -e dev react-scripts build",
    "prod": "env-cmd -e prod react-scripts start",
    "build-prod": "env-cmd -e prod react-scripts build",
    "staging": "env-cmd -e staging react-scripts start",
    "build-staging": "env-cmd -e staging react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  
 ```

## once setup is done in `package.json` run command.

## Development

`npm run dev`

`npm run build-dev`

## Staging

`npm run staging`

`npm run build-staging`


## Production

`npm run prod`

`npm run build-prod`
