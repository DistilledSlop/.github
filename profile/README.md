# DistilledSlop

We build Minecraft bots, run them in isolated worlds, and turn their network traffic into data for learning experiments. The projects here connect task planning and pathfinding with fleet operation, recording, and model training.

## Projects

| Project | What it does |
| --- | --- |
| [Vibrato](https://github.com/DistilledSlop/Vibrato) | Minecraft automation built on AltoClef and Baritone, with task planning and gameplay behaviors. |
| [Baritone](https://github.com/DistilledSlop/Baritone) | Our Baritone fork, with movement, navigation, and recovery changes for Vibrato. Development lives on `vibrato-engine`. |
| [Vibrato Conductor](https://github.com/DistilledSlop/Vibrato-Conductor) | Runs fleets of isolated Minecraft workers, assigns collection tasks, and retains captures and diagnostic evidence. |
| [Protocol Transformer](https://github.com/DistilledSlop/Protocol-Transformer) | Records Minecraft packets, builds typed token datasets, and experiments with training models to generate client actions. |

## How the pieces fit

Vibrato uses our Baritone fork to act in the world. Conductor manages the workers and collection runs. Protocol Transformer records the traffic and provides the dataset, training, and inference pipeline.

The collection and learning stack targets **Minecraft Java 1.21.1**. Protocol Transformer is experimental research code; its current model does not yet outperform an always-idle baseline.

Start with [Vibrato](https://github.com/DistilledSlop/Vibrato) for the bot, [Conductor](https://github.com/DistilledSlop/Vibrato-Conductor) for fleet operation, or [Protocol Transformer](https://github.com/DistilledSlop/Protocol-Transformer) for the learning pipeline. Each repository has its own setup instructions.

## Built on

Vibrato continues [AltoClef](https://github.com/gaucho-matrero/altoclef) and uses [Baritone](https://github.com/cabaletta/baritone). Credit to their authors and contributors for the foundations. Each repository retains its own license and upstream history.
