NO_PUBKEY problem for Intel SGX repo:

```ssh
cloudsigma@sgx:~$ sudo apt-get update 
Hit:1 http://archive.ubuntu.com/ubuntu jammy InRelease
Hit:2 http://archive.ubuntu.com/ubuntu jammy-updates InRelease                                     
Hit:3 http://archive.ubuntu.com/ubuntu jammy-backports InRelease                                   
Hit:4 http://security.ubuntu.com/ubuntu jammy-security InRelease    
Get:5 https://download.01.org/intel-sgx/sgx_repo/ubuntu jammy InRelease [1236 B]
Err:5 https://download.01.org/intel-sgx/sgx_repo/ubuntu jammy InRelease
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY E5C7F0FA1C6C6C3C
Reading package lists... Done
W: GPG error: https://download.01.org/intel-sgx/sgx_repo/ubuntu jammy InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY E5C7F0FA1C6C6C3C
E: The repository 'https://download.01.org/intel-sgx/sgx_repo/ubuntu jammy InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```
Downloading and using key file in sources.list didn't help.

Solution:

```ssh
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E5C7F0FA1C6C6C3C
```

Get the fingerprint:
```ssh
sudo apt-key fingerprint
Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
/etc/apt/trusted.gpg
--------------------
pub   rsa2048 2023-03-20 [SC] [expires: 2027-03-20]
      1504 34D1 488B F803 08B6  9398 E5C7 F0FA 1C6C 6C3C
uid           [ unknown] CN=Intel(R) Software Development Products

/etc/apt/trusted.gpg.d/ubuntu-keyring-2012-cdimage.gpg
------------------------------------------------------
pub   rsa4096 2012-05-11 [SC]
      8439 38DF 228D 22F7 B374  2BC0 D94A A3F0 EFE2 1092
uid           [ unknown] Ubuntu CD Image Automatic Signing Key (2012) <cdimage@ubuntu.com>

/etc/apt/trusted.gpg.d/ubuntu-keyring-2018-archive.gpg
------------------------------------------------------
pub   rsa4096 2018-09-17 [SC]
      F6EC B376 2474 EDA9 D21B  7022 8719 20D1 991B C93C
uid           [ unknown] Ubuntu Archive Automatic Signing Key (2018) <ftpmaster@ubuntu.com>
```
Use fingerprint for `signed-by`:

```
cloudsigma@sgx:~$ cat /etc/apt/sources.list.d/intel-sgx.list
deb [signed-by=150434D1488BF80308B69398E5C7F0FA1C6C6C3C arch=amd64] https://download.01.org/intel-sgx/sgx_repo/ubuntu jammy main
```
