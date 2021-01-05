## Ubuntu

## SSH-Agent

# start SSH-Agent
ubuntu@dlp:~$ eval $(ssh-agent)
Agent pid 983

# add Identity
ubuntu@dlp:~$ ssh-add
Enter passphrase for /home/ubuntu/.ssh/id_rsa:
Identity added: /home/ubuntu/.ssh/id_rsa (/home/ubuntu/.ssh/id_rsa)

# confirm
ubuntu@dlp:~$ ssh-add -l
2048 xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:4c:b2 /home/ubuntu/.ssh/id_rsa (RSA)

# try to conenct with SSH without passphrase
ubuntu@dlp:~$ ssh www.srv.world hostname
www.srv.world

# exit from SSH-Agent
ubuntu@dlp:~$ eval $(ssh-agent -k)
Agent pid 983 killed

## SSH

## SSH-Agent

ssh -A ubuntu@192.168.0.1 -i /home/ubuntu/.ssh/id_rsa_company

