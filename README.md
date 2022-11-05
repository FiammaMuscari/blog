## Agregando Eslint en next

Eslint viene preinstalado en Next asi que lo iniciamos

### Tener en Preferencias

 configuración > .json
```bash
"editor.codeActionsOnSave": {
        "source.fixAll.eslint": true 
    }
}
```

Iniciamos:

```npx eslint --init```

### Agregar plugin

``` npm add --dev eslint-plugin-react@latest eslint-config-standard@latest eslint@^8.0.1 eslint-plugin-import@^2.25.2 eslint-plugin-n@^15.0.0 eslint-plugin-promise@^6.0.0``` 

En https://nextjs.org/docs/basic-features/eslint#migrating-existing-config hay mas info

También agregamos
```npm install --save-dev @next/eslint-plugin-next```

## actualizar module
```bash
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": [  
        "plugin:react/recommended",
        "standard",
        "plugin:@next/next/recommended"
    ],
    "overrides": [
    ],
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "plugins": [
        "react",
        "react-hooks"
    ],
    "rules": {
      "react-hooks/rules-of-hooks": "error",
      "react-hooks/exhaustive-deps": "warn",
      "react/prop-types":"off",
      "react/react-in-jsx-scope":"off"
    }
}
```

Listo, al guardar con Ctrl + s se acomodan solos los archivos.


## Getting Started Nextjs

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
