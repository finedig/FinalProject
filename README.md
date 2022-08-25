# Martial Arts Combo Recognition

 This image recognition network can recognize a moving set of martial arts strikes and pair them into combos from a video input.

## The Algorithm

1. It initializes the keras model and prepares the network
2. For each frame, it resizes it to 224 x 224 for more efficiency
3. It predicts what each frame is
4. To prevent false positives, only certain items are added to the superList
   i. The average of the last two confidence levels is taken
   ii. If it is greater than 90% and the classes are the same
   iii. It is then added to the superList
5. The refineList function gets rid of the repeat values in the superList
6. The splitCombos function turns
   i. The "nothing" class into nothing
   ii. The "end" class into the end of a combo mini list
   iii. Removes empty lists
7. The superList (now supremeList) is printed with all of the combos listed in order
8. Voila! The code is complete.

## Running this project

1. Install and open 'martial_arts_combo_recognition.py'
2. Install all images marked 'frame(#)' and the keras model
3. Replace <MODEL_FILEPATH> with the file path of the model
4. Replace <IMAGE_FILEPATH> with the file path of the image folder
5. Correct the number of frames to the amount of images installed
7. Run the code! (It will output a list of combos if done correctly)

Installation Instruction Video
https://youtu.be/XiufgtHluj0
