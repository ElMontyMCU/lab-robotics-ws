# Lab Robotics Workspace

Workspace de ROS 2 para el proyecto de robótica de laboratorio: un robot móvil
Clearpath Husky que patrulla puntos y un brazo UR5e para pick & place, ambos en simulación.

## Requisitos

- Ubuntu 24.04
- ROS 2 Jazzy
- Gazebo Harmonic

## Instalación y compilación

Desde la raíz del repositorio:

```bash
# Cargar ROS 2 (underlay): necesario antes de compilar
source /opt/ros/jazzy/setup.bash

# Solo la primera vez en cada máquina
sudo rosdep init

# Instalar dependencias
rosdep update
rosdep install --from-paths src --ignore-src -y

# Compilar
colcon build --symlink-install
```

## Uso

Cargar el workspace (overlay) en cada terminal nueva, después del underlay:

```bash
source /opt/ros/jazzy/setup.bash
source install/setup.bash
```

Lanzar el sistema principal:

```bash
# Pendiente: el launch principal todavía no existe.
```

## Tests

```bash
colcon test
colcon test-result --verbose
```