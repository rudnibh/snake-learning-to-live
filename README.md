# Snake: Learning to Live

This project implements a reinforcement learning agent that learns to play the classic Snake game. The agent is trained using deep Q-learning and interacts with a custom Snake environment.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/35f8148d-55f4-4fae-8344-260ebd363e5d" />


## Features
- Custom Snake game environment
- Deep Q-learning agent
- Model saving and loading
- Modular codebase for easy experimentation

## Project Structure
- `game.py`: Contains the Snake game logic and environment.
- `agent.py`: Implements the reinforcement learning agent.
- `model.py`: Defines the neural network model used by the agent.
- `helper.py`: Utility functions for training and gameplay.
- `model/`: Directory for storing trained model weights (`model.pth`).

## Getting Started

### Prerequisites
- Python 3.7+
- Recommended: Create a virtual environment

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/rudnibh/snake-learning-to-live
   cd snake-learning-to-live
   ```
2. (Optional) Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
To train the agent or play the game, run:
```bash
python agent.py
```


## Model
- Trained models are saved in the `model/` directory as `model.pth`.
- You can load a pre-trained model for evaluation or further training.

### Loading a Saved Model

To load a saved model in your code, use the following example:

```python
import torch
from model import Linear_QNet

# Adjust input_size, hidden_size, output_size as per your model definition
model = Linear_QNet(input_size, hidden_size, output_size)
model.load_state_dict(torch.load('model/model.pth'))
model.eval()  # Set the model to evaluation mode
```

Replace `input_size`, `hidden_size`, and `output_size` with the appropriate values used during training.

