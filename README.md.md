### 1. Hyperparameters settings of Baselines

##### For the selection of hyperparameters, we follow the SimPO's work (https://github.com/princeton-nlp/SimPO.). For the ODPO_alpha, we follows the fefault settings in ODPO' paper (http://arxiv.org/abs/2402.10571)

- **Mistral-7B**

| Methods | beta | λD/λU | ODPO_alpha | SimPO_gemma_beta | LR   | Batch Size |
| ------- | ---- | ----- | ---------- | ---------------- | ---- | ---------- |
| KTO     | 0.01 | 1.0   | /          | /                | 5e-7 | 64         |
| SImPO   | 2.0  | /     | /          | 0.8              | 5e-7 | 64         |
| ODPO    | 0.01 | /     | 1.0        | /                | 5e-7 | 64         |

- **Llama3-8B**

| Methods | beta | λD/λU | ODPO_alpha | SimPO_gemma_beta | LR   | Batch Size |
| ------- | ---- | ----- | ---------- | ---------------- | ---- | ---------- |
| KTO     | 0.01 | 1.0   | /          | /                | 5e-7 | 64         |
| SImPO   | 2.0  | /     | /          | 0.5              | 5e-7 | 64         |
| ODPO    | 0.01 | /     | 1.0        | /                | 5e-7 | 64         |

### 2. Convergence visualization of DPO and TODO considering different tie data ratios in train set.



- **Mistral**

  - Total loss changes during training phase of DPO and TODO
  
  ![Total loss changes of Mistral-7B aligned with DPO and TODO](figs\mistral_total_loss_00.png)
  
  
  - Preference loss changes during training phase of DPO and TODO
  
  ![Total loss changes of Mistral-7B aligned with DPO and TODO](figs\mistral_preference_loss_00.png)
  
- **Llama 3**

  - Total loss changes during training phase of DPO and TODO
  
  ![Total loss changes of Llama3-8B aligned with DPO and TODO](figs\llama_total_loss_00.png)
  
  
  - Preference loss changes during training phase of DPO and TODO
  
  ![Total loss changes of Llama3-8B aligned with DPO and TODO](figs\llama_preference_loss_00.png)