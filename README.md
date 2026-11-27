# G1 stair locomotion with TD-regularized PPO

Stair ascent and descent for the Unitree G1 humanoid in MuJoCo, comparing standard PPO with TD-regularized PPO (Parisi et al., 2019), as a basis for online policy improvement from deployment experience.

Plan:

1. **Simulation pretraining.** A MuJoCo stair environment with a curriculum (flat → single step → ascent → descent → harder geometry) and domain randomization; PPO vs TD-regularized PPO under identical budgets.
2. **Online adaptation in simulation.** Update the pretrained actor and critic from new experience under controlled mismatches in friction, actuators, mass and sensing.
3. **Supervised trials on the physical G1**, if stage 2 is validated.

Builds on a flat-ground G1 walking benchmark: [g1-humanoid-walking](https://github.com/TeodorPenchev04/g1-humanoid-walking).

Work in progress.

## Setup (macOS)

```bash
python3.11 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
# MuJoCo Menagerie next to this repo:
git clone --depth 1 https://github.com/google-deepmind/mujoco_menagerie.git ../mujoco_menagerie
```
