# Rover4We
A simple 4-wheeled rover with differential traction and ackerman steering for MuJoCo physics engine (MJCF model)

### Files
rover4We-only.xml is only the rover, without a floor. Meant to be included (imported) in other file.
rover4We-field.xml is a floor with the rover included.

#### rover4We-only
The model implements both ackerman steering geometry and rear differential drive.
* first one is done with equality constraints between the ```ghost-steering-wheel``` (like a steering wheel, visible over the rover) and both the front wheels (```f-r-wheel``` and ```f-l-wheel```).
* last one is done with a motor attached to a fixed tendon (http://www.mujoco.org/book/XMLreference.html#fixed) that is coupled with both rear wheels (```r-r-wheel``` and ```r-l-wheel```)

Many thanks to Emo Todorov's answer on this MuJoCo's Forum thread: http://www.mujoco.org/forum/index.php?threads/implement-differential-drive-in-mujoco.3367/#post-3620

This resource can also provide a help to this thread: http://www.mujoco.org/forum/index.php?threads/any-plan-to-release-a-simple-car-model.3751/#post-5633

