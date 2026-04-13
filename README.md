
### 1. Generate the SSH Key

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

### 2. Add the Key to the SSH Agent


```bash
eval "$(ssh-agent -s)"
```

```bash
ssh-add ~/.ssh/id_ed25519
```

### 3. Add the Public Key to GitHub


```bash
cat ~/.ssh/id_ed25519.pub
```


### 4. Test the Connection


```bash
ssh -T git@github.com
```

