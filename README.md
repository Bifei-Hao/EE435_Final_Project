# EE435 Final Project: Video Generation and Enhancement with E2VID and ELIC


## Run E2VID

- Download the pretrained model:

```bash
wget "http://rpg.ifi.uzh.ch/data/E2VID/models/E2VID_lightweight.pth.tar" -O pretrained/E2VID_lightweight.pth.tar
```

- Download an example file with event data:

```bash
wget "http://rpg.ifi.uzh.ch/data/E2VID/datasets/ECD_IJRR17/dynamic_6dof.zip" -O data/dynamic_6dof.zip
```
- Run reconstruction:

```bash
python run_reconstruction.py \
  -c pretrained/E2VID_lightweight.pth.tar \
  -i data/dynamic_6dof.zip \
  --auto_hdr \
  --display \
  --show_events
```
## Run Elic

code of ELic is in $\texttt{EE435.ipynb}$, follow the code.







This code borrows from the following open source projects, whom we would like to thank:

```bibtex
@Article{Rebecq19pami,
  author        = {Henri Rebecq and Ren{\'{e}} Ranftl and Vladlen Koltun and Davide Scaramuzza},
  title         = {High Speed and High Dynamic Range Video with an Event Camera},
  journal       = {{IEEE} Trans. Pattern Anal. Mach. Intell. (T-PAMI)},
  url           = {http://rpg.ifi.uzh.ch/docs/TPAMI19_Rebecq.pdf},
  year          = 2019
}
```
```
@inproceedings{he2022elic,
  title={Elic: Efficient learned image compression with unevenly grouped space-channel contextual adaptive coding},
  author={He, Dailan and Yang, Ziming and Peng, Weikun and Ma, Rui and Qin, Hongwei and Wang, Yan},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={5718--5727},
  year={2022}
}
```
