Assignment 4: due March 17 (11:59 pm)

In this assignment, you will experiment with various types of recurrent neural networks (RNNs) and transformers in PyTorch.


Download the base code for this assignment:

Part 1: cs480_winter23_asst4_char_rnn_classification.ipynb

Part 2: cs480_winter23_asst4_char_rnn_generation.ipynb

Part 3: cs480_winter23_asst4_seq2seq_translation.ipynb


Answer the following questions by modifying the base code in each notebook. Submit the modified Jupyter notebooks via LEARN.


Part 1 (5 points): Encoder implementation in cs480_winter23_asst4_char_rnn_classification.ipynb. Compare the accuracy of the encoder when varying the type of hidden units: linear units, gated recurrent units (GRUs) and long short term memory (LSTM) units. For linear hidden units, just run the script of the Jupyter notebook as it is. For GRUs and LSTMs, modify the base code. Save the following results in your Jupyter notebook:

Two graphs that each contain 3 curves (linear hidden units, GRUs and LSTM units). The first graph displays the training loss and the second graph displays the validation loss. In both graphs, the y-axis is the negative log likelihood and the x-axis is the number of thousands of iterations.

For each type of hidden unit, print the test loss and the test confusion matrix of the model that achieved the best validation loss among all iterations (i.e., one best test loss and test confusion matrix per type of hidden unit).

Explanation of the results (i.e., why some hidden units perform better or worse than other units).


Part 2 (5 points): Decoder implementation in cs480_winter23_asst4_char_rnn_generation.ipynb. Compare the accuracy of the decoder when varying the information fed as input to the hidden units at each time step: i) previous hidden unit, previous character and category; ii) previous hidden unit and previous character; iii) previous hidden unit and category; iv) previous hidden unit. For i), just run the Python notebook as it is. For ii) and iv) modify the code to feed the category as input to the hidden unit(s) of the first time steps only. For iii) and iv), modify the code to avoid feeding the previous character as input to each hidden unit. Save the following results in your Jupyter notebook:

Two graphs that each contain 4 curves (i, ii, iii, iv). The first graph displays the training loss and the second graph displays the validation loss. In both graphs, the y-axis is the negative log likelihood and the x-axis is the number of 500 iterations.

For each architecture, print the test loss of the model that achieved the best validation loss among all iterations (i.e., one best test loss per architecture).

Explanation of the results (i.e., how does the type of information fed to the hidden units affect the results).

Part 3 (5 points): Seq2seq implementation in cs480_winter23_asst4_seq2seq_translation.ipynb. Compare the accuracy of RNN seq2seq models with and without attention as well as a transformer. To keep the running time reasonable, use a hidden_size of 32 (in practice, a hidden size of at least 512 would be used, but for the purpose of this assignment, use 32). Test the translation models on sentences of MAX_LENGTH = 5 and 10. For the RNN seq2seq model with attention (hidden_size=32 and MAX_LENGTH=5), just run the base code as it is. For the RNN seq2seq model without attention, modify the base code to call the DecoderRNN class (without attention) already provided. For the transformer model, use the nn.TransformerEncoder, nn.TransformerDecoder or nn.Transformer classes in the PyTorch library and modify any part of the base code that you see fit. Set the parameters of the transfomer to match those of the RNN see2seq models whenever possible (i.e., d_model=32), otherwise feel free to choose suitable parameters. Save the following results in your Jupyter notebook:

Four graphs that each contain 3 curves (RNN seq2seq with attention and RNN seq2seq without attention and transformer). The first and second graphs display the training loss and the validation loss respectively for sentences of MAX_LENGTH=5. The third and fourth graphs display the training loss and validation loss respectively for sentences of MAX_LENGTH=10. In all graphs, the y-axis is the negative log likelihood and the x-axis is the number of thousands of iterations.

For each architecture tested with sentences of MAX_LENGTH=5, print the test loss of the model that achieved the best validation loss among all iterations (i.e., one best test loss per architecture). Similarly, for each architecture tested with sentences of MAX_LENGTH=10, print the test loss of the model that achieved the best validation loss among all iterations (i.e., one best test loss per architecture).

Explanation of the results (i.e., how does the attention and architecture of each model affects the results?).
