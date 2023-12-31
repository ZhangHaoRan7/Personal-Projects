In this project we are trying to build a classifier that distinguishes images of Martian terrain with frost. You can find the dataset in https://dataverse.jpl.nasa.gov/dataset.xhtml?persistentId=doi:10.48577/jpl.QJ9PYA.
This dataset was created to study Mars’ seasonal frost cycle and its role in theplanet’s climate and surface evolution over the past 2 billion years. The data helps in identifying low-latitude frosted microclimates and their impact on climate.

i. Images (png files) and labels (json files) are organized in the data directory by “subframes.” Subframes are individual 5120x5120 pixel images which are
crops of the original HiRISE images (often on the order of 50k x 10k pixels).
Individual subframes were annotated by the contributors and then sliced into 299x299 “tiles.” Each tile has an associated label for use in training ML
algorithms. There are 214 subframes and a total of 119920 tiles. Each tile has annotations which have been used to assign labels to the tiles ‘frost’ or ‘background.’
Each JSON file contains all the annotation information collected from human annotators.

Image tiles are organized into folders of ‘background’ and ‘frost’ classes (binary). For the purpose of the final project, individual tiles shall serve as the
data points which need to be classified using binary classification.
ii. The dataset includes files for splitting the data into train, test and validation.
However, we were provided by an improved version of those files when a repo is created:
A. train source images.txt
B. test source images.txt
C. val source images.txt

iii. Each of these files contains the IDs of the high rise images (parent folders forthe subframes and tiles).

1. By parsing folder structures and extracting information from specific files, the intelligent loading of image data is achieved, accompanied by necessary data preprocessing and normalization. Subsequently, the data is methodically split into predefined training, validation, and test sets.

2. Leveraging the TensorFlow framework, a convolutional neural network (CNN) model is ingeniously constructed, with meticulous definition of relevant training parameters to ensure optimal learning capabilities and generalization performance.

3. The training process of the CNN model is initiated using the model.fit function, incorporating an early stopping strategy to dynamically monitor the loss on the validation set, enhancing training efficiency and the model's robustness.

4. The trained model is comprehensively evaluated on the test set, and a detailed classification report is generated, encompassing key performance metrics such as accuracy, recall, and F1 score.

5. Transfer learning is implemented by employing pre-trained models such as EfficientNetB0, ResNet50, and VGG16. Through strategically freezing specific neural network layers, extracting high-level feature representations, and ultimately constructing a new model for further training, this process facilitates more rapid and effective model training in similar domains or tasks.