
<br/>
<h1>on AWS Ec2 make server compatible for deployment</h1>

## first update your default packages --> `sudo apt-get update`
## first update your default packages --> `sudo apt-get upgrade`
### check weather git is installed or not --> `type git` or `git --veresion` (if not installed)
## install git --> `sudo apt install git`
## check git version again --> `git --veresion`


<br/>
<h1>now we have to install node</h1>

<li>got to this website and get the which version you want to install just copy and paste to terminal -- "https://github.com/nodesource/distributions#debian-and-ubuntu-based-distributions"</li>
<li>check the latest version and replace yum to apt</li>

## check node installed or not --> `node -v`
## check npm installed or not --> `npm -v`


<br/>
<h1>now clone git repo</h1>

## install node_modules --> `npm i`
## check local app is running or not --> `npm run dev`
## check production is running on local or not --> `npm run preview`

<br/>
## if want to install serve `sudo npm install --global serve`
## check app is serving or not  `serve`
make security group available for custom port 3000 or what port you want
## make serve build  `serve -s build/dist`

<br/>
<h1> now we want to keep our server ready for everytime or background -- need of pm2 </h1>

## install pm2   `sudo npm install pm2 -g`
## run server   `pm2 serve build/dist 80 --spa`
## check server   `pm2 ls`
## check errors   `pm2 logs`
## delete server   `pm2 delete servername`
## other pm2 command --> 

`pm2 status`
`pm2 restart all`
`pm2 stop all`
`pm2 logs`
`pm2 flush` (clear logs)
