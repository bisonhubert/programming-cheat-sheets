# [Code Push CLI](https://github.com/Microsoft/code-push/blob/master/cli/README.md#getting-started)

![codepush-commands](https://cloud.githubusercontent.com/assets/116461/16246693/2e7df77c-37bb-11e6-9456-e392af7f7b84.png)

```bash
install codepush cli
$ npm i -g code-push-cli
```

```bash
register codepush account
$ code-push register
```

```bash
log out of codepush
$ code-push logout
```

```bash
see who you're currently registered as
$ code-push whoami
```

```bash
uninstall codepush cli
$ npm uninstall -g code-push-cli
```

```bash
view list of connected apps
$ code-push app list
```

```bash
rollback latest release
$ code-push rollback ProMobile-Android QA
$ code-push rollback ProMobile-Android Staging
$ code-push rollback ProMobile-IOS QA
$ code-push rollback ProMobile-IOS Staging
```

```bash
view deployment history
$ code-push deployment history ProMobile-IOS Production
$ code-push deployment ls ProMobile-IOS
```


