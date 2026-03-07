# Node.js Proc

Makes it easy to run child processes when the nodejs `node:child_process` module is available.

```ts
const repoHasChanges = await proc('git status', { cwd: '/path/to/my/repo' }).then(({ output }) => {
  return output[has]('working tree clean');
});
```

By default no environment vars are passed to `proc`. To pass environment vars, use:
```ts
await proc('my command', { env: process.env });
```