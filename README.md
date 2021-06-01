
# wally_description

Este pacote se trata da versão virtual do robô Wally

<p align="center">
    <img src="./figs/WALLY_FINAL.png" width="600" height="360" title="Wally Robot">
</p> 

## Instruções

##### 1. Instalar todos os pacotes necessários:

```sh
$ sudo apt-get install ros-kinetic-gmapping
$ sudo apt-get install ros-kinetic-xacro
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-gazebo-ros-pkgs
$ sudo apt-get install ros-kinetic-Gazebo-ros-control
$ sudo apt-get install ros-kinetic-joy
$ sudo apt-get install ros-kinetic-teleop-twist-keyboard
$ sudo apt-get install ros-kinetic-teleop-twist-joy
$ sudo apt-get install ros-kinetic-navigation
```

##### 2. Criando o catking workspace:

```sh
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src
$ catkin_init_workspace
```

##### 3. Faça o download deste pacote para a pasta src do seu catkin workspace:

```sh
$ git clone https://github.com/GerbersonFelix/wally_description.git
$ cd ..
$ catkin_make
```

##### 4. Abrindo o ambiente de simulação:

```sh
$ cd ~/catkin_ws/
$ source devel/setup.bash
$ roslaunch wally_description wally.launch
```

##### 5. Para controlar via teclado:

```sh
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
##### 6. Para controlar via joystick:

```sh
$ rosrun joy joy_node
$ rosrun teleop_twist_joy teleop_node
```

##### 7. Para fazer mapeamento:

```sh
$ roslaunch wally_description gazebo_mapping_robot.launch
```

##### 8. Para salvar um mapa:

```sh
$ cd ~/catkin_ws/src/wally_description/maps
$ rosrun map_server map_saver -f nomedomapa
```
##### 9. Para iniciar a simulação com o mapa salvo:

```sh
$ roslaunch wally_description gazebo_map_robot.launch 
```
##### 10. Para iniciar a simulação com o world de teste:

```sh
$ roslaunch wally_description gazebo_teste.launch
```

## Avisos

#**Se der erro com algum launch, verificar o caminho dos arquivos dentro do arquivo do launch.**
#**Para controle e odometria do Wally instale [este](https://github.com/GerbersonFelix/wally_control_odom) pacote.**
