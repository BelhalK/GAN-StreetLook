# ACTIVATE TORCH
. /Users/karimimohammedbelhal/torch-cl/install/bin/torch-activate

# TO TRAIN
DATA_ROOT=myimages dataset=folder th main.lua

With display = 0 and gnu = 0

# TO GENERATE
gpu=0 batchSize=64 net=checkpoints/experiment1_25_net_G.t7 th generate.lua

With net being the last Generator checkpoint


gpu=0 batchSize=1 imsize=10 noisemode=linefull net=checkpoints/experiment1_25_net_G.t7 th generate.lua


# RENAME ALL IMAGES

rename -e 's/.*/photo-$N.jpg/' *.jpg
rename -e 's/.*/street-$N.jpg/' *.jpg

# DISPLAY UI
th -ldisplay.start