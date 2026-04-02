# Welcome to My User Page
*By Samuel Zubatiy*

[Skip down to my Lab Checklist](#course-checklist)

## About Me
I am a student at UCSD and I am **highly motivated** to learn software engineering this quarter in CSE 110. Outside of school I *love* to go surfing and just spend time at the beach.

> "It's not that I'm so smart, it's just that I stay with problems longer." - Albert Einstein

[Click here to view my profile picture directly](profile.jpg)

[Click here to view my project's README file](README.md)

## My Technical Skills
Here is a snippet of code I like from my parallel computing class last quarter. This is the process of computing a convolution when you have different input images, output images, 2D elements in each, different masks, and 2D elements in that mask:

```c
void convLayer_forward(int B, int M, int C, int H, int W, int K, float* x, float* k, float* y)
{
    int H_out = H - K + 1;
    int W_out = W - K + 1;

    for (int b = 0; b < B; b++)             // for each image in batch
        for(int m = 0; m < M; m++)          // for each output feature map
            for(int h = 0; h < H_out; h++)  // for each output element
                for(int w = 0; w < W_out; w++) {
                    y[b, m, h, w] = 0.0f;
                    for(int c = 0; c < C; c++)      // sum over all input feature maps (channels)
                        for(int p = 0; p < K; p++)  // KxK filter
                            for(int q = 0; q < K; q++)
                                y[b, m, h, w] += x[b, c, h + p, w + q] * k[m, c, p, q];
                }
}

Here are my favorite computer science classes ranked:
1. CSE 30
2. CSE 101
3. CSE 29

Here are my favorite tools:
* AWS
* Git
* Arduino IDE
* Fusion 360

## Let's Connect
I am always looking to expand my network. 
[Connect with me on LinkedIn](https://www.linkedin.com/in/samzubatiy/)

## Course Checklist
Here is what I need to accomplish for CSE 110 to go smoothly:
- [x] Reinstall VS Code since I have been recently using Cursor
- [x] Refamiliarize myself with git since I haven't used it in a few months now
- [x] Create my first .md file
- [ ] Understand why software engineering is not all about coding
- [ ] Connect with Professor Powell more