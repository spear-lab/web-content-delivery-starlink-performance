[![](https://img.shields.io/badge/WWW'26-Paper-blue)]()

  
  

# Investigating Web Content Delivery Performance over Starlink

  

This is the artifacts repository of the Web Conference (WWW) 2026 paper: Investigating Web Content Delivery Performance over Starlink


## 📖 Abstract
Low Earth Orbit (LEO) satellite ISPs promise universal Internet connectivity, yet their interaction with content delivery remains poorly understood. We present the first comprehensive measurement study decomposing Starlink’s web content delivery performance decomposed across Point of Presence (PoP), DNS, and CDN layers. To quantify how satellite architecture disrupts terrestrial CDN assumptions, we conduct a measurement study spanning two years. We identify three distinct performance regimes based on infrastructure density. Regions with local content-rich PoPs achieve near-terrestrial latencies with the satellite segment dominating 80–90% of RTT. Infrastructure-sparse regions suffer cascading penalties: remote PoPs force distant resolver selection, which triggers CDN mislocalization, pushing latencies beyond 200 ms. Dense-infrastructure regions show minimal sensitivity to PoP changes. Leveraging Starlink’s infrastructure expansion in early 2025 as a natural experiment, we demonstrate that relocating PoPs closer to user location reduces median page-fetch times by 60%. Our findings reveal that infrastructure proximity, not satellite coverage, influences web performance, requiring fundamental changes to CDN mapping and DNS resolution for satellite ISPs.

## 📝 Reference 
```
@inproceedings{cdnperformance-starlink-www26,
	title={{Investigating Web Content Delivery Performance over Starlink}},
  	author={Bose, Rohan and Zhao, Jinwei and Shreedhar, Tanya and Pan, Jianping and Mohan, Nitinder},
	year = {2026}, 
	publisher = {Association for Computing Machinery}, 
	address = {New York, NY, USA}, 
	booktitle = {Proceedings of the Web Conference 2026},
	series = {WWW '26}
}
```
  
  ## 💾 Dataset

The data necessary for the plots needs to be downloaded before starting and is available at [mediaTUM](https://mediatum.ub.tum.de/1840504) with instructions on how to set it up. 
After unzipping the dataset, please make sure the "dataset folder" is setup in the same directory.

## 📊 Reproducibility Instructions
All plots were created with Python3.9.6. We recommend following our instructions to create a virtual Python environment with the package versions that we used.

```
git clone https://github.com/spear-lab/web-content-delivery-starlink-performance.git
cd web-content-delivery-starlink-performance
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter nbconvert --to=html --execute starlink_cdn_performance_analysis.ipynb
```