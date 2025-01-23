# Environment

```bash
# 먼저 CUDA toolkit API 버전이 12.1 이어야 함.
conda create -n ngp2 python==3.11
conda install pytorch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 pytorch-cuda=12.1 -c pytorch -c nvidia


# 외부 라이브러리를 설치해줘야 함.


cd raymarching
# $PROJ_ROOT/raymarching/setup.py <- 이새끼 문제가 있음.
# setup.py 에서 nvcc_flags 의 -std=c++14 옵션을 -std=c++17 로 수정
python setup.py install


cd gridencoder
# $PROJ_ROOT/gridencoder/setup.py <- 이새끼도 문제가 있음.
# setup.py 에서 nvcc_flags 의 -std=c++14 옵션을 -std=c++17 로 수정
python setup.py install

shenencoder

sh ./scripts/install_ext.sh

```