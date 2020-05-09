# Detection-of-dubious-database
 A company has hired agents to sign up clients for them. These agents are paid based on the number of clients they register. As such, they have registered one clients more than once. Data scientists have been employed to help fish out these dubious clients
PROOF OF CONCEPT
As a data scientist, I solved the problem using two models.
The first model fishes out the clients that have been registered more than once in the dubious database. I called this model "DOUBLE FACE DETECTION CLUSTERING MODEL".
The second model checks if a new client already exists in the rectified database before he or she is added. I called this model "VERIFY NON-EXISTENCE OF NEW CLIENTS".

First model
This model uses the clustered image of the individual images of the clients in the dubious system. Thus, clients "NTLC001-NTLC007". After the necessary libraries are loaded, the clustered image of the individual clients is loaded as the input image.CorelDraw helps to get this clustered image. The model then finds the individual faces in the clustered image and encodes each of them uniquely into a 128 vector. After saving the individual faces and encoded images in empty lists, the clustering process then begins.
Unique cluster folders according to the number of clusters detected are being created and the images of clients being registered more than once are detected and stored in the unique folders.
After you apply this model on our dataset, thus the individual mugshots of the clients, it’ll detect the following pair to be the same:
NTC 001 & NTLC003
NTLC002 & NTLC 007
NTLC004 & NTLC006
This means only NTLC005 was not registered more than once and the therefore the following clients have to be the only clients in the rectified databases:
NTLC001
NTLC002 
NTLC004
NTLC005
After this has been done, the second model takes over. Intricate explanation of the model has been added as a video in the link below.

Second  model
The second model detects the existence of new clients in the rectified database before they are being added. First the model is being trained with the mugshots of the unique clients that have been updated in the system and assigned to the known names in the rectified database. These are the names the model will print if the new client that Npontu is trying to add is already in the database. If the client is not in the rectified database, the model will print “Unknown Person”.
Intricate explanation of the model has been added as a video to the link below.


ATTACHMENTS
The attachments of the solution are the relevant information that was used in the pipe flow. These include:
clients.jpg - The clustered image of the original clients in the dubious database.(“NTLC001 - NTLC007”).
clients.cdr - The coreldraw file that shows how the clustered image was obtained. The video explains the process in detail.
frameimage.jpg - The image with rectangles on it indicating the individual detected faces before the clustering is done.
NTLC001.jpg - NTLC007.jpg - The original clients in the dubious database
Part1.mp4 - part4.mp4 - The video explaining the whole solution in intricate details.
new_clients.jpg - The updated image after a new client “TRIAL 2” was added.
TRIAL1, TRIAL2, TRIAL3 - The new images that were used to ascertain whether the second model was working. After “TRIAL 2” was detected as “Unknown Person”, the rectified database was updated and the coreldraw clients.jpg was updated to new_clients.jpg.
NPONTU DATABSE.xlsx - The combination of dubious database and the rectified database on different spreadsheets.
DOUBLE FACE DETECTION CLUSTERING MODEL.ipynb - The first model
VERIFY NON-EXISTENCE OF NEW CLIENTS.ipynb - The second model
relevant folder - contains images that were used for didactic purposes in the video.
Newcluster - contains the uniquely clustered folders containing the clients in the database that were registered more than once.

