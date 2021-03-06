# FlowNet2 TensorFlow Setup:
This includes FlowNet2, C, S, CS, CSS, CSS-ft-sd, and SD.

**NOTE: We use flownet2 for all our experiments.**


### Installation
```
pip install enum
pip install pypng
pip install matplotlib
pip install image
pip install scipy
pip install numpy
pip install tensorflow
```

Linux:
`sudo apt-get install python-tk`

You must have CUDA installed:
`make all`

### Download weights
To download the weights for all models (4.4GB), run the `download.sh` script in the `checkpoints` directory. All test scripts rely on these checkpoints to work properly. 
If the download fails, directly download the weights from [here](https://doc-0g-b4-docs.googleusercontent.com/docs/securesc/diuhiier8f3lbm44v9p44d1n6o10ft4n/nog1d2rv5rt7lh5iam2669nd7t55p979/1529805600000/18093896044146087554/18093896044146087554/1B4Mdy2m_FPqSC16Z0LPsmsZaa-H9rTZD?e=download&h=09221738537919217220&nonce=mqtog9d488cog&user=18093896044146087554&hash=ft9ejlhjrrvlaotcnput6vo62fmgmfn2) and unzip in `checkpoints` folder.

### Testing: 
```
python -m src.flownet2.test --input_a data/samples/frame_0001.png --input_b data/samples/frame_0001.png --out /data/samples/out/ --outname 1and2
```

Available models:
* `flownet2`
* `flownet_s`
* `flownet_c`
* `flownet_cs`
* `flownet_css` (can edit test.py to use css-ft-sd weights)
* `flownet_sd`

### References
[1] E. Ilg, N. Mayer, T. Saikia, M. Keuper, A. Dosovitskiy, T. Brox
FlowNet 2.0: Evolution of Optical Flow Estimation with Deep Networks,
IEEE Conference in Computer Vision and Pattern Recognition (CVPR), 2017.
[2] Sampepose's FlowNet2-tf Implementation: https://github.com/sampepose/flownet2-tf
