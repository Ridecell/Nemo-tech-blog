Motivation:

Rule based algorithms have been replaced by machine learning networks which 

ML better than rule based for many applications spcly where we have a lot of data collected.
However, ML fails for systems where we do not have enough data or an anomaly is seen in production/inference time.
Talk of how most often the training samples are curated, how test set could have cases never seen before. Give examples - a wheelchair on road might not have been trained for during our roadside object detection network and if such thing is seen on the road, our detector fails to detect it as object which could lead to major accident! A forklift or a deer on the road, might not be present in our curated training samples but could happen in deployment/real world.

Application:

Factory/Manufacturing industry:
Factory line has many objects and each factory industry has its own product/by products or raw materials inside the field. Annotating every object on the site is not only difficult but also very inefficient. For major purposes, we don’t need to identify the class of the object accurately. As long as we are able to categorize it into one of the vehicles, stationary parts or movable parts, majority of our factory problems gets easier.

AV/ADAS:
Road accidents form one of the major fatalities in the world. AV and ADAS companies have been trying to curb the situation by either assisting the drivers or replacing them with more robust algorithms. However, one problem with these robust solutions is despite being more accurate than a human in detecting objects which might be similar to the ones it has been trained on, it performs worse than a human for scenarios or objects it has not seen before. If we want to replace humans from the loop completely, we need to make our systems reliable and atleast as accurate as humans in terms of analyzing the scenario and determining the object. Here again, we do not care if the human or the system is able to identify the object accurately, as long as it identifies the object and is able to predict its behavior based on that, that is sufficient for it to be able to navigate. We need a solution which could identify the novel object on the road scene through its attributes such as whether it is a vehicle or a stationary object or 



Open Set Recognition network:

In our paper “Don’t just YOLO: Reason What You See!, we encourage our readers to see one step beyond! We humans, from our childhood, learn to make some associations between any new object we come across to one or combination of objects we have seen in our past. Those associations are based on the properties of each object which help us define it a category. Most supervised-ly trained networks fail in these attempts which could be fatal if they are meant to replace humans in the loop. Image 1 illustrates how easy it is for humans to classify those objects as vehicles as opposed to any sophisticated supervised-ly trained network.

Through our paper, we propose a novel yet simple solution where we reason any object instance/class as a collection of common and shareable representations in 2D feature space. When the object instance is seen or known during train time, most of the features and their respective locations in 2D space is known whereas any novel unseen/unknown object during inference, shared features are lesser with more of unknown features and the object contains more uncertainties. We define a cost function to the end during inference which determines if the object has been seen during train time or not, if not, it uses feature similarities to reason the

Model architecture:
	
	

