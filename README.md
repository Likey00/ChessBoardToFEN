# ChessBoardToFEN
Project which uses PyTorch to classify Digital Chess Boards into their FEN notation

## Steps to use final classifier
- Upload "best_model_cpu_scripted.pt" and "PredictNewBoard.ipynb" to your Google Drive
- Run "PredictNewBoard.ipynb" in Google Colab
- Take a snip of the board you want to classify (Should be close to the exact board square)
- Upload the image file using the file upload button to see the predicted FEN!

## How I built the final classifier
- I started with the various chess boards with labeled FENs found at https://www.kaggle.com/datasets/koryakinp/chess-positions
- I split the first 1000 boards into labeled tiles for training in "process.ipynb".
- I zipped my labeled tiles and sent them to Google Drive, then trained a model to predict them in "IdentifyChessPieces.ipynb"
- I stored my best model in Google Drive, and tested my model's accuracy on the full boards in "PredictBoardFENs.ipynb"
- I stored the CPU version of my model, and made the final board prediction tool in "PredictNewBoard.ipynb"
