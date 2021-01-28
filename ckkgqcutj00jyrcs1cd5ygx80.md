## 📨 Setup Postfix w/ SPF verification

send bulk emails like a pro on your own using `postfix`

## ⚙ Installation

```
sudo apt install postfix mailutils
```

###  📝 adding SPF record to your DNS 
```txt
xyz.com. 1799 IN TXT "v=spf1 ip4:x.x.x.x a mx ~all"
```

### 🔧 Commands

#### ✉ Sending test mail
```sh
echo "body" | mail -s "subject" -a "From: Harsh Z <sender@example.com>" receiver@example.com
```

#### 📤 Check Mail Queue
```sh
mailq
```

#### 🗑 Clear Mail Queue
```sh
postsuper -d ALL
```

### ✅ Verifying Mail in Gmail
1. Open Email
2. More (three dots on top right)
3. Show Original
4. Look for SPF (Pass with IP x.x.x.x) 

### 🧰 Google Toolbox
https://toolbox.googleapps.com/apps/dig/

