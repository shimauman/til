## Version
- 

## Before
```
// Access to EC2 instance with SSH.
$ ssh -i path-to-file-written-secret-access-key-or-pem-file ec2-user@ip-address-of-the-instance -p port-number
```

## After
```
$ ssh sample
```

## How To
1. Go to `.ssh` directory.
```
$ cd ~/.ssh
```
2. Edit `.ssh/config`
```
$ vim config
```
```
// ~/.ssh/config

Host sample
  HostName ip-address-of-the-instance
  User ec2-user
  IdentityFile path-to-file-written-secret-access-key-or-pem-file
  Port port-number
```
3. Put secret access key on new directory
```
// On .ssh directory

$ mkdir aws
$ chmod 700 aws
$ cd aws
$ touch sample
$ chmod 600 sample
```
4. Write secret access key on the file

```
// ~/.ssh/aws/sample

-----BEGIN RSA PRIVATE KEY-----
***
-----END RSA PRIVATE KEY-----
```

## Other Use Case
- Access to GitHub with SSH

## Reference
- [Qiita : .ssh/configでSSH接続の管理](https://qiita.com/0084ken/items/2e4e9ae44ec5e01328f1)
