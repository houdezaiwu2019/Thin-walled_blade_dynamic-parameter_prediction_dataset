## Thin-walled blade dynamic-parameter prediction dataset

### Input

The input of the network is the blade geometric information tensor converted from the 3D model.   Considering the thin-walled structure of the blade, blade geometric information tensor is compressed into a form similar to the picture-like tensor which is formed by stacking several 2D matrices.  

![data_preprocess](pic/data_preprocess.png)

Then, the nine normalized 256 × 256 matrices are stacked in turn to obtain the 256 × 256 × 9 tensor, called the geometric tensor. 

The specific data is in the `dataset/geo`, where the tensor data is stored in the format of `.npy`.

### Output

Output of the network is the modal information, i.e., the first five mode shapes and natural frequencies of the blade. 

The output mode shape can be converted into a tensor similar to the shape of the input geometric information tensor, and the output frequency can be converted into a vector after above process. The mode shape is a 256 × 256 × 5 tensor, 



![github_dataset](pic/github_dataset.png)

The natural frequency is a 1 × 5 vector, 