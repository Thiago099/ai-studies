
The gradient descent solve the problem of transofrming x into y, however it has many layers in between. I do undesthant what happen in the last layer, however after that, I don't know exactly how it is optimized. All i can think is that the derivative can find a good solution because the noise that is generated in the weight and bias values. I believe i was misunderstood about how it works, however if that is not the case, what is happening that is very inefficient.
If that is the case, maybe diffusion models work well because they the x - y conversion happens more times, making the model more efficient.
All of this came to my mind while I was creating a diffusion model for studying purposes. Instead of timestamp encoding I went for a more simple solution of separating my model into chunks training each chunk separately then joining them together. And then came the thought, on this diffusion model I had a clear x and y for each layer group making it a lot more efficient than if I train all the layers together. After iv done with 100 iterations for each chunk, I trained the full model for another 100 iterations with the x been the random noise y the denoised output, and it got worse. Here is a comparasion


![image](https://github.com/Thiago099/ai-studies/assets/66787043/62174482-9da7-47ce-ba32-0d4d83e7e3d6)



100 more epochs after the network was joined




![image](https://github.com/Thiago099/ai-studies/assets/66787043/75dc64bc-385f-4590-8567-d2d177336ba2)


What I believe is happening is that averaging similar or even all images of the same class has a higher score than generating extra detail
Here is the notebook with the diffusion model i created:
https://github.com/Thiago099/ai-studies/blob/main/diffusion.ipynb
I'm probably misunderstanding something, and I would like some clarification so I can become a better programmer.
