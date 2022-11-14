Steps to reproduce:

```
yarn
yarn dev
```

- Open http://localhost:3000. You will see all your HTTP headers e.g. `user-agent`.
- Open http://localhost:3000/qwe. You will see only one fake header: `{ "host": "localhost" }`
