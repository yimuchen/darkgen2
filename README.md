# darkgen2

First-time installation instructions (`-p` for Pythia8.226, `-e` for HepMC, `-d` for Delphes):
```
mkdir scratch
cd scratch
git clone git@github.com:kpedro88/darkgen2
./darkgen2/setup.sh -p -e -d
cd darkgen2
source init.(c)sh
make pythiaTree
```

Environment setup instructions (every time):
```
cd scratch/darkgen2
source init.(c)sh
```

To run `pythiaTree` executable (where `[card]` is one of the `.cmnd` text files):
```
./pythiaTree.exe [card]
```

To run Delphes on the output:  
```
DelphesHepMC delphes_card_CMS_imp.tcl haha.root hepmc.out
```

To analyze results from Delphes:
```
root -l 'emgD.C("haha.root")'
```
