
# wally_description

Este pacote se trata da versão vitual do robô Wally

<p align="center">
    <img src="./figs/Wally.png" width="600" height="360" title="Wally Robot">
</p> 

## Instruções

##### 1. Instalar todos os pacotes necessários:

```sh
$ sudo	apt-get	install	ros-kinetic-gazebo-ros-pkgsros-kinetic-Gazebo-ros-control
$ sudo	apt-get	install	ros-kinetic-teleop-twist-keyboard
```

##### 2. Criando o catking workspace:

```sh
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
catkin_init_workspace
```

##### 3. Faça o download deste pacote para a pasta src do seu catkin workspace:

```sh
$ git clone https://github.com/GerbersonFelix/wally_description.git
$ cd ..
$ catkin_make
```

##### 4. Descompacte os meshes

```sh
$ cd ~/catkin_ws/src/wally_description/meshes
$ unzip base_link.STL.zip && unzip rp_lidarA1.stl.zip
```

##### 5. Abrindo o ambiente de simulação:

```sh
$ cd ~/catkin_ws/
$ source devel/setup.bash
$ roslaunch wally_description wally.launch
```

##### 6. Para controlar via teclado

```sh
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
