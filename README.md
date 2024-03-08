### Efforts Relating to the Installation and Testing of TopFit

So the TopFit repo provides information on how to install eUniRep and UniRep. They want you to build the conda environment
using a file called **protein_fitness_prediction.yml** which will yield a lot of conflicts due mostly to the fact they have
a lot of older versions of the modules. Here is how you can create the necessary environment working. At least at worked 
for me. Of course, further testing will be needed.

1) Get protein_fitness_prediction.yml from [THIS repo](https://raw.githubusercontent.com/Ortlund-Laboratory/topfit/main/protein_fitness_prediction). I've edited it accordingly
  
2) Set and export the variable

```
$ SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True
$ export SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL
```

3) Execute the following:

```
conda env create -f protein_fitness_prediction.yml
```

4) Activate the environment

```
$ conda activate protein_fitness_prediction
```

5) Run the following commands to get the torch stuff installed

```
$ pip install torchaudio==0.5.0 torchvision==0.6.0+cu101 torch==1.5.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```

