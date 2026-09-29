# 01 - Server, locked door, page online

## What I did
Launched an Ubuntu EC2 instance on AWS in ap-southeast-5,
gave it a fixed Elastic IP, hardened the SSH config, then
installed Nginx and served my own page on port 80.

## Architecture in one line
Browser -> Elastic IP -> security group -> Nginx.

## Commands I used
    sudo sshd -T | grep -iE 'passwordauth|permitroot'
    sudo sshd -t && sudo systemctl restart ssh
    sudo apt install nginx -y
    sudo nginx -t && sudo systemctl enable --now nginx

    ## What went wrong and how I fixed it
<WRITE-ONE-LINE-HERE>

## One thing I learned
<WRITE-ONE-LINE-HERE>

## Note
Training lab; server and IP recycled after the session.
Screenshots show it live. IPs written <YOUR-ELASTIC-IP>.
## Where things live
Nginx config: /etc/nginx/sites-available/default
Access log:   /var/log/nginx/access.log
