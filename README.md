# Run it on Colab

Follow these steps to run the code on Google Colab:

1. Clone the repository:
   ```bash
   !git clone https://github.com/Aadit778/Single_SuperRes.git
2. Install the required dependencies:
   ```bash
   !pip install -r /content/Single_SuperRes/requirements.txt

3. Run the application:
   ```bash
   %cd Single_SuperRes
   !python /content/Single_SuperRes/app.py --colab
## **Test the Model**

To test the model, use the following command:

```bash
!python inference.py -i [input folder] -o [output folder] --scale 4 --ckpt weights/SinSR_v1.pth --one_step --chop_size 256 --task SinSR

```

To test the model with Ground Truth, use the following command:
```bash
!python inference.py -i testdata/imagenet256/lq/ -o results/SinSR/imagenet  -r testdata/imagenet256/gt/ --scale 4 --ckpt weights/SinSR_v1.pth --one_step --chop_size 256 --task SinSR
