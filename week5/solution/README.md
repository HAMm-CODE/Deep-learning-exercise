# Exercise 5 Solution: Machine Translation with Transformers

This folder contains the completed solution for Exercise 5, including the notebook and the artifacts produced during training and inference. It is organized so an interviewer can quickly review the workflow, reproduce results, and verify outputs.

## What This Contains

- ex5.ipynb: The full solution notebook with data preparation, model definition, training, and autoregressive inference.
- model.pth: Trained model weights saved after training.
- translation.npy: Saved translated token sequences produced during inference.

## Workflow Overview

1. Data preparation and tokenization using the provided CSVs.
2. Vocabulary construction with special tokens (<PAD>, <SOS>, <EOS>).
3. Transformer model implementation and training.
4. Autoregressive translation and artifact export.

## How To Run

1. Open ex5.ipynb and run cells in order.
2. Update the dataset path so it points to the dataset_ex5 folder.
3. Train the model. If you already have weights, set skip_training = True.
4. Run the translation cell to produce translation.npy.

## Notes For Review

- The translation loop is autoregressive and stops on <EOS> or max length.
- The notebook saves model weights and translations for submission.
- Keep the notebook cells intact; some are used for hidden tests.

## Sample Output

original_sentence: new jersey est parfois calme pendant l' automne.
translated_sentence: new jersey is sometimes quiet during fall <EOS>
----------
original_sentence: california est generalement calme en mars.
translated_sentence: california is usually quiet during march <EOS>
----------
