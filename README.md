# based-node-red-iot-dashboard
基于node-red  esp8266 dht11 arduino ide 的一个简单物联网仪表盘教程

## 运行截图
<img src="https://github.com/YUNXISO/based-node-red-iot-dashboard/blob/master/img/%E8%BF%90%E8%A1%8C%E6%88%AA%E5%9B%BE1.png" />

## 节点图
<img src="https://github.com/YUNXISO/based-node-red-iot-dashboard/blob/master/img/%E8%8A%82%E7%82%B9%E5%9B%BE.png" />

## emqx 安装

sudo yum install -y yum-utils device-mapper-persistent-data lvm2

sudo yum-config-manager --add-repo https://repos.emqx.io/emqx-ce/redhat/centos/7/emqx-ce.repo

sudo yum install emqx

emqx start

## node js 安装
curl -sL https://rpm.nodesource.com/setup_10.x | bash -

yum install -y nodejs

node -v
npm -v

## node red 安装
sudo npm install -g --unsafe-perm node-red

## 后台运行
nohup node-red &

## node red设置密码

npm install bcryptjs
打开setting 取消注释
node -e "console.log(require('bcryptjs').hashSync(process.argv[1], 8));" 你要设置的密码

## 导入节点
[{"id":"f4d41aa0.5c9338","type":"function","z":"92dad0c6.b117d","name":"Temperature","func":"msg.payload = msg.payload.value.Temperature\nreturn msg;","outputs":1,"noerr":0,"x":510,"y":280,"wires":[["98a325e9.054fc8","3c5fde92.9d0622","f4a3867e.166e48"]]}]
