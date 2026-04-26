
### 1. Generate the SSH Key

```bash
ssh-keygen -t ed25519 -C "raniv2057@gmail.com"
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

### 5. Clone Local Manifests

Choose the branch you want to build and run the corresponding command to clone the local manifests:

**For Infinity:**
```bash
git clone git@github.com:Rexons-AOSP-Projects/topaz_manifest.git -b infinity .repo/local_manifests
```

**For Axion:**
```bash
git clone git@github.com:Rexons-AOSP-Projects/topaz_manifest.git -b axion .repo/local_manifests
```

**For Lunaris:**
```bash
git clone git@github.com:Rexons-AOSP-Projects/topaz_manifest.git -b lunaris .repo/local_manifests
```

**For Mist:**
```bash
git clone git@github.com:Rexons-AOSP-Projects/topaz_manifest.git -b mist .repo/local_manifests
```

**For Evolution:**
```bash
git clone git@github.com:Rexons-AOSP-Projects/topaz_manifest.git -b evolution .repo/local_manifests
```
