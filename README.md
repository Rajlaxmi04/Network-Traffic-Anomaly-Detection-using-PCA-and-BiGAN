# Network Traffic Anomaly Detection using PCA and BIGAN


## Prerequisites.
To run the code, follow those steps:

Install Python 3

```
sudo apt install python3 python3-pip
```
Download the project code:

```
git clone https://github.com/Rajlaxmi04/Network-Traffic-Anomaly-Detection-using-PCA-and-BiGAN
```
Install requirements (in the cloned repository):

```
pip3 install -r requirements.txt
```

## Doing anomaly detection.

Running the code with different options

```
python3 main.py <bigan> <kdd> run --nb_epochs=<number_epochs> --label=<0, 1, 2, 3, 4, 5, 6, 7, 8, 9> --w=<float between 0 and 1> --m=<'cross-e','fm'> --d=<int> --rd=<int> --nc=<int>
```
To reproduce the results of the paper, please use w=0.1 (as in the original AnoGAN paper which gives a weight of 0.1 to the discriminator loss), d=1 for the feature matching loss.  

Example command is shown below. Here nc is PCA n_components. Set to 28 for best performance results
python main.py bigan kdd run --nb_epochs=10 --w=0.1 --m=cross-e --d=1 --nc=28


Courtesy: https://arxiv.org/pdf/1802.06222.pdf
Original code was modified by applying PCA to the dataset
