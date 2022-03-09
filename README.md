# Object Visualization

Visualization for Object Matching. Static objects are coloured in white, removed ones in red, novel ones in green and displaced ones in pink (an arrow points from the old location to the new one).

## 1. build and run docker container

`https://github.com/Sasha-ObjectMatching-Pipeline/object_visualization.git`

```
cd object_visualization_service/docker
docker build -t "vis" . 
run ./sh
```


## 2. Start mongodb

`roslaunch --wait mongodb_store mongodb_store.launch db_path:=/path/to/mongodb`

## 3. Start Visualization program
`rosrun object_visualization_service visualization.py`

## 4. Controll Visualization program via services

Publish Pointcloud: `rosservice call /object_visualization_service/visualize`

Clear Pointcloud: `rosservice call /object_visualization_service/clear`

Stop Publish Pointcloud: `rosservice call /object_visualization_service/stop`


