# Physics-Informed and Hybrid Machine Learning in Additive Manufacturing: Application to Fused Filament Fabrication
Physics-based models are used to inform the deep learning models to better predict the quantity of interests.

## Abstract 
This article investigates several physics-informed and hybrid machine learning strategies that incorporate physics knowledge in experimental data-driven deep-learning models for predicting the bond quality and porosity of fused filament fabrication (FFF) parts. Three types of strategies are explored to incorporate physics constraints and multi-physics FFF simulation results into a deep neural network (DNN), thus ensuring consistency with physical laws: (1) incorporate physics constraints within the loss function of the DNN, (2) use physics model outputs as additional inputs to the DNN model, and (3) pre-train a DNN model with physics model input-output and then update it with experimental data. These strategies help to enforce a physically consistent relationship between bond quality and tensile strength, thus making porosity predictions physically meaningful. Eight different combinations of the above strategies are investigated. The results show how the combination of multiple strategies produces accurate machine learning models even with limited experimental data.

## Cite Paper
Kapusuzoglu, Berkcan, and Sankaran Mahadevan. "Physics-Informed and Hybrid Machine Learning in Additive Manufacturing: Application to Fused Filament Fabrication." JOM (2020): 1-11.
Please, cite this repository using: 
	
	
	@article{berkcan2020PIML,
	  title={Physics-Informed and Hybrid Machine Learning in Additive Manufacturing: Application to Fused Filament Fabrication},
	  author={Kapusuzoglu, Berkcan and Mahadevan, Sankaran},
	  journal={JOM},
	  pages={1--11},
	  year={2020},
	  doi={[https://doi.org/10.1007/s11837-020-04438-4](https://link.springer.com/article/10.1007/s11837-020-04438-4#article-info)},
	  publisher={Springer}
	}
	
## notebooks
DataGeneration: Generates and saves data.
	1. Loop over measured data (bond length and porosity)
	2. Loop over temperature evolution results from simulations and predict neck growth and porosity for synthetic data (physics-based).

PorosityPredictions: Predict porosity & bond length using Physics-based models (Temperature data is obtained using the analytical solution for transient heat conductions for 25 sets of parts stored in \data\ModelData)


## data
labeled_data -> results
unlabeled_data -> results (1519 samples)


1. supervised
	- temperature (simulations)
	- experiment
2. unsupervised
	- temperature (simulations for 1519 synthetic data)
		-- "temperature/syntheticdata/" (temperature evolution for 25 synthetic data with similar inputs as used in expeirments)
	- simulation (process parameters for synthetic data)
		-- SyntheticData: 25 parts representing 25 experiments
		-- Parts: 1519 parts representing random synthetic data
		
## Results
1. results
	- Sintering model developed by BK
