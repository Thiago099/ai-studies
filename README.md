the gradient descent solve the problem of transofrming x into y, however it has many layers in between. i do undesthant what happen in the last layer, however after that i dont know anything about how it learns, all i can think is that it is solved by the noise that is generated in the weight and bias values. I believe I'm misunderstanding about how it works, if not what is happening that is very inefficient.
If that is the case, maybe diffusion models work well because they the x - y conversion happens more times, making the model more efficient.

All of this came to my mind while I was creating a diffusion model for studying purposes. Instead of timestamp encoding I went for a more simple solution of separating my model into chunks training each chunk separately then joining them together. And then came the thought, on this diffusion model I had a clear x and y for each layer group making it a lot more efficient than if I train all the layers together. After iv done with 100 iterations for each chunk, I trained the full model for another 100 iterations with the x been the random noise y the denoised output, and it got worse. Here is a comparasion

Image generated by the separated training
![image](https://github.com/Thiago099/ai-studies/assets/66787043/9e7bf830-d25a-4a59-a034-f19218b51f8f)

Separated training
![image](https://github.com/Thiago099/ai-studies/assets/66787043/75dc64bc-385f-4590-8567-d2d177336ba2)

Separated training
100 more epochs after the network was joined

Here is the notebook with the diffusion model i created:
https://github.com/Thiago099/ai-studies/blob/main/diffusion.ipynb
I'm probably misunderstanding something, and I would like some clarification so I can become a better programmer.
