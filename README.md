# rmbug/packages

Package repository for rmBug — served at https://packages.rmbug.com

## apt (Debian / Ubuntu)

```bash
curl -fsSL https://packages.rmbug.com/apt/gpg.asc | sudo gpg --dearmor -o /usr/share/keyrings/rmbug.gpg
echo "deb [signed-by=/usr/share/keyrings/rmbug.gpg] https://packages.rmbug.com/apt stable main" | sudo tee /etc/apt/sources.list.d/rmbug.list
sudo apt-get update && sudo apt-get install rmbug-agent
```

## yum / dnf (RHEL / Fedora / Amazon Linux)

```bash
sudo rpm --import https://packages.rmbug.com/yum/gpg.asc
sudo tee /etc/yum.repos.d/rmbug.repo << 'EOF'
[rmbug]
name=rmBug
baseurl=https://packages.rmbug.com/yum
enabled=1
gpgcheck=1
gpgkey=https://packages.rmbug.com/yum/gpg.asc
EOF
sudo dnf install rmbug-agent
```

Packages are updated automatically on each agent release.
