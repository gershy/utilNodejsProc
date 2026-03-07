# Node.js Proc

Makes it easy to run child processes when the nodejs `node:child_process` module is available.

```ts
const repoHasChanges = await proc('git status', { cwd: '/path/to/my/repo' }).then(({ output }) => {
  return output[has]('working tree clean');
});
```