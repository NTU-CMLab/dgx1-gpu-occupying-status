# dgx1-gpu-occupying-status
Show GPU occupying status in dgx-1 (using nvidia-smi)

## Requirement

- `nvidia-smi`
- A dgx-1 environment(docker based)

## Usage

```bash
$ gpu-status.sh 
```

## Sample output

```
Total GPUs: 8
Avalible GPUs: 2
 
GPU_serial      Porcess_id      Container_name          Process_name
======================================================================================
0323616134471   18567           /big_pike               python model_cvpr_dgx.py 
0323716019841   29383           /b02902054_tf           python -u tf_seqs2seq_model.py
0323716019841   6684            /b02902054_tf           python -u tf_seqs2seq_model.py 
0323716019794   18784           /r05944047_gan2         ./build/tools/caffe train --solver=./face_solver.prototxt -gpu=3,4 
0323716019794   1130            /r05922005-crn          python train_crn3d.py 
0323716019809   18784           /r05944047_gan2         ./build/tools/caffe train --solver=./face_solver.prototxt -gpu=3,4 
0323716019809   51266           /r05922005-crn          python train_crn3d.py --data perturbed 
0323616133931   43952           /r03922007_MTK          python3 -u MTK-Flickr-exp-G2-4/TF.py 
0323716019820   70648           /r03922007_MTK          python3 -u EXP-G1/LPGAN-exp-G1-8/TF.py 
```
