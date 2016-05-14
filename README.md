```
pip install https://storage.googleapis.com/tensorflow/mac/tensorflow-0.5.0-py2-none-any.whl # for mac
pip install https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.5.0-cp27-none-linux_x86_64.whl # for ubuntu
```

1. Grabs parallel data.
2. Gets train, dev split.
3. Builds vocabulary
4. Converts parallel data into ids

From the root directory:

```
python -m tensorshake.get_data
python -m tensorshake.prepare_corpus
```

Delete /cache to start anew.

## Train

Use the example BASH script to train the model. This saves the check points in the `--train_dir` directory.
If you run it again, the training process continues from the check point. To restart with fresh parameters,
simply delete/rename the check points.

```
./run.sh
```

## Possible improvements

- word embeddings
- beam search
- language model reranking
