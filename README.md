# Meta-RL: Episodic/Contextual and Incremental Two-Step Task (PyTorch)

In this repository, I reproduce the results of [Prefrontal Cortex as a Meta-Reinforcement Learning System](https://www.nature.com/articles/s41593-018-0147-8)<sup>1</sup>, [Episodic Control as Meta-Reinforcement Learning](https://www.biorxiv.org/content/10.1101/360537v2)<sup>2</sup> and [Been There, Done That: Meta-Learning with Episodic Recall](https://arxiv.org/abs/1805.09692)<sup>3</sup> on variants of the sequential decision making "Two Step" task originally introduced in [Model-based Influences on Humans’ Choices and Striatal Prediction Errors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3077926/)<sup>4</sup>. You will find below a description of the task along with a brief overview of Meta-RL, as well as details covering the structure of the code.

<table align="center">
    <tr>
        <th>Episodic Two-Step Task</th>
        <th>Episodic LSTM</th>
    </tr>
    <tr>
        <td align="center" width="50%"><img alt="Two-Step Task Illustration" src="assets/episodic_task.png"></td>
        <td align="center" width="50%"><img alt="Episodic LSTM" src="assets/episodic_lstm.png"></td>
    </tr>
</table>


*I aim to write a blog post to accompany this repository, so stay tuned!

## Overview of Meta-RL

## The Two-Step Task

### Incremental 

### Episodic/Contextual

## Results

<table align="center">
    <tr>
        <th>Published Result</th>
        <th>My Result</th>
    </tr>
    <tr>
        <td align="center" width="50%"><img alt="Stay Prob Two-Step Task Published" src="assets/published_twostep_stayprob.png"></td>
        <td align="center" width="50%"><img alt="Stay Prob Two-Step Task" src="assets/twostep_stayprob.png"></td>
    </tr>
</table>

## Code Structure

## References

1. Wang, J., Kurth-Nelson, Z., Kumaran, D., Tirumala, D., Soyer, H., Leibo, J., Hassabis, D., & Botvinick, M. (2018). [Prefrontal Cortex as a Meta-Reinforcement Learning System](https://www.nature.com/articles/s41593-018-0147-8). *Nat Neurosci*, **21**, 860–868.
2. Ritter, S., Wang, J., Kurth-Nelson, Z., & Botvinick, M. (2018). [Episodic Control as Meta-Reinforcement Learning](https://www.biorxiv.org/content/10.1101/360537v2). *bioRxiv*.

3. Ritter, S., Wang, X., Kurth-Nelson, Z., Jayakumar, M., Blundell, C., Pascanu, R., & Botvinick, M. (2018). [Been There, Done That: Meta-Learning with Episodic Recall](https://arxiv.org/abs/1805.09692). *ICML*, 4351–4360. 

4. Daw, N. D., Gershman, S. J., Seymour, B., Dayan, P., & Dolan, R. J. (2011).[Model-based Influences on Humans’ Choices and Striatal Prediction Errors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3077926/). *Neuron*, 69(6), 1204–1215. https://doi.org/10.1016/j.neuron.2011.02.027


5. Mnih, V., Badia, A.P., Mirza, M., Graves, A., Lillicrap, T., Harley, T., Silver, D. & Kavukcuoglu, K.. (2016). [Asynchronous Methods for Deep Reinforcement Learning](https://arxiv.org/abs/1602.01783). Proceedings of The 33rd International Conference on Machine Learning, in *PMLR* 48:1928-1937

## Acknowledgments

I would like to give a shout out to the repositories and blog posts that were of great help to me when implementing this project. Make sure to check them out!

- https://github.com/qihongl/dnd-lstm 
- https://github.com/mtrazzi/two-step-task
- https://github.com/lnpalmer/A2C 
- https://github.com/rpatrik96/pytorch-a2c
- https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html 