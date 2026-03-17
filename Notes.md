https://github.com/googlecreativelab/quickdraw-dataset/blob/master/README.md#get-the-data

https://quickdraw.readthedocs.io/en/latest/

import tensorflow as tf

gcs_path = 'gs://your-bucket-name/your-file.csv'
local_path = './your-file.csv'
tf.io.gfile.copy(gcs_path, local_path, overwrite=True)

Which form of data do we want?
Simplified, Numpy bitmaps, Raw files, binary
