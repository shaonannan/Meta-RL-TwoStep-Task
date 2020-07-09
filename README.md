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

In recent years, deep reinforcement learning (deep-RL) have been in the forefront of artificial intelligence research since DeepMind's seminal work on DQN <sup>5</sup> that was able to solve a wide range of Atari games by just looking at the raw pixels, as a human would. However, there remained a major issue that disqualified it as a plausible model of human learning, and that is the sample efficieny problem. It basically refers "to the amount of data required for a learning system to attain any chosen target level of performance" <sup>6</sup>. In other words, a task that would take a biological brain a matter of minutes to master would require many orders of magnitude more training data for a deep-RL artificial agent. Botvinick et al. (2019) <sup>6</sup> identify two main sources of slowness in deep-RL: the need for *incremental paramter adjustment* and starting with a *weak inductive bias*. I will be going into more details of each in my blog post. However, they note that subsequent research has shown that it is possible to train artificial agents in a sample efficient manner, and that is by (1) augmenting it with an episodic memory system to avoid redundant exploration and leverage prior experience more effectively, and (2) using a meta-learning approach by training the agent on a series of structurally interrelated tasks that can strengthen the inductive bias (narrowing the hypothesis set) which enables the agent to hone-in to a valid solution much faster <sup>6</sup>.

### Connection with Neuroscience

DeepMind have been preaching about the importance of neuroscience and artifcial intelligence research to work together in what they call a virtuous circle; where each field will inspire and drive forward the other <sup>7</sup>. I must admit that they were the reason I joined an MSc program in Computational Cognitive Neuroscience after working on AI for a couple of years now. In short, they were indeed able to show that meta-RL - which was drawn from the machine learning literature - is able to explain a wide range of neuroscientific findings as well as resolve many of the prevailing quandaries in reward-based learning <sup>1</sup>. They do so by conceptualizing the prefrontal cortex along with its subcortical components (basal ganglia and thalamic nuclei) as its own free standing meta-RL system. Concretely, they show that dopamine driven synaptic plasticity, that is model free, gives rise to a second more efficient model-based RL algorithm implemented in the prefrontal's network activation dynamics <sup>1</sup>. In this repository, I reproduce one of their simulations (the two-step task) that showcases the emergence of model-based learning in accord with observed behavior in both humans <sup>?</sup> and rodents <sup>?</sup>. 

The episodic meta-RL variant was proposed by Ritter et al. (2018) <sup>?</sup> and is partly inspired by evidence that episodic memory retrieval in humans operate through reinstatement that recreates patterns of activity in neural circuits supporting working memory <sup>?</sup>. This presents a new theory in which human decision making can be seen as an interplay beween working and episodic memory, that is itself learned through training to maximise rewards on a distribution of tasks. This will be expanded upon as well in the accompanied blog post. 

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