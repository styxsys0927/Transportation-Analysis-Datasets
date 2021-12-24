# Transportation-Analysis-Datasets
Collections of datasets for different traffic analysis tasks

## Traffic forecasting
### Static sensors (does not include camera or radar data)
For forcasting tasks, the dataset usually contain two parts: a list of features detected by each sensors every k minitues (shape=[T*k minitues,N detectors, F features], k is usually 5 and F is usually 1) and an adjacent matrix of size N*N. The adjacent matrix is usually generated from geographical distances between detectors.
- **METR-LA:** Los Angeles freeway data. Can be found at https://github.com/liyaguang/DCRNN. We employ the pre-processed version at https://github.com/Fanglanc/DKFN (1 month * 207 sensors). 
- **Seattle Inductive Loop Detector Dataset:** See details at https://github.com/zhiyongc/Seattle-Loop-Data (2 months * 323 sensors).
- **INRIX traffic network:** The dataset is used in https://arxiv.org/ftp/arxiv/papers/1802/1802.07007.pdf. One may apply for authority at https://docs.inrix.com/ for more data.
- **PeMS:**  Performance Measurement System (PeMS) is a system (https://pems.dot.ca.gov/) providing traffic data collected by California Department of Transportation (Caltrans). 
  - PeMS-S
  - PEMS-BAY: bay area freeway data. Can be found at https://github.com/liyaguang/DCRNN (4 months * 325 sensors).
  - PeMSD4
  - PeMSD7: the district covering LA county. There are more than 8000 sensors (by 2019) in this district. A subset of this dataset can be acquired at https://github.com/VeritasYin/STGCN_IJCAI-18 (2 months * 228 sensors only on weekdays).
  - PeMSD8: the district covering San Bernadino county. We extracted 1 month * 1150 sensors speed and occupancy data. The adjacent maitrix is created based on distance and travel direction (we assume that sensors on opposite directions are not connected).

- **BJER4 (no resource):** east ring No.4 routes in Beijing City. Details can be found in https://www.ijcai.org/proceedings/2018/0505.pdf. 

### Regional traffic flow (does not include camera or radar data)
Compute inflow and outflow of regions at each timestamp.
- **ride-hailing Dataset:** not clearly stated in https://ojs.aaai.org//index.php/AAAI/article/view/4247. 
- **DidiSY (no resource):** collected by the authors of https://arxiv.org/pdf/1905.10069v1.pdf. 
- **BikeNYC:** might be this one https://ride.citibikenyc.com/system-data. Not clearly stated in https://arxiv.org/pdf/1610.00081.pdf. 
- **TaxiBJ:** can be acquired here https://github.com/TolicWang/DeepST/tree/master/data/TaxiBJ. data shape: (7220, 2, 32, 32) = (time, in/outflow, subregionX, subregionY)
- **UCAR (no resource):** See https://github.com/Zekun-Cai/GEML-Origin-Destination-Matrix-Prediction-via-Graph-Convolution for details.
- **Didi:** Acquired from https://github.com/Zekun-Cai/GEML-Origin-Destination-Matrix-Prediction-via-Graph-Convolution. See https://github.com/Zekun-Cai/GEML-Origin-Destination-Matrix-Prediction-via-Graph-Convolution for details.
- **Xiamen:** https://ieeexplore.ieee.org/document/8029849 mentions a webcite which no longer response.
### Parking lot
- **Beijing & Shenzhen:** https://ojs.aaai.org/index.php/AAAI/article/view/5471 mentions an API without further explaination.

### Point of interest (POI)
OpenStreetMap
### Camera data
See https://github.com/fjchange/awesome-video-anomaly-detection.
