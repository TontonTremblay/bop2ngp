# BOP 2 NGP json
convert annotation from https://bop.felk.cvut.cz/home/ to make it compatiable with NGP transform.json. In the scene folder of BOP, this scripts add `transforms.json` that can be passed to NGP. This script assumes there is only one object in the scene, please see the script to add more objects. 

There are a couple options: 
- `path` where is the data, it is expecting the path to the train folder in bop format. 
- `make_alpha` do you want to make a new folder to add the mask of the object, this is the format that makes the best results. 
- `only_alpha_trans` This will not generate the masks images (it can take a while), but the data will be refered to the masked images. (In case you need to re-run the script)
- `debug` This uses meshcat to run visualize the camera poses. Please run `meshcat-server` if you run with this debug. 