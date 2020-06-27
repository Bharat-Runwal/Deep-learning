# Image Captioning(Using CNN encoder and RNN decoder)
- Firstly,downloading the data(COCO)would require a lot of space 20GB.
- CNN Encoder: Pre trained InceptionV3 model and used its last hidden layer as an embedding, Feature extraction would take time.

- Captions: Captions are converted to indices using voabulary(voacab is extracted from train_captions),Padding is done to ensure each sentence have same indices length."START"
 and "END" tokens are inserted at start and end of each sentence respectively. 

- Image features extracted from CNN encoder is used as an initial state for LSTM instead of zeros.
- During training we will feed ground truth tokens into lstm to get predictions of next tokens.
- To reduce the number of parameters Bottlneck approach is used.
## Final Model
-We take an image as an input and embed it
- Condition lstm on that embedding
- Predict the next token given a START input token
- Use predicted token as an input at the next time step
- Iterate until we predict an END token
