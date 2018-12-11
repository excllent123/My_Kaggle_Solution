# My_Kaggle_Solution

Human Protein Atlas Image Classification

#Todolist:

1 HPA data

2 lr with warm start

3 带权重采样

model = nn.Linear(10, 2)
optimizer = optim.SGD(model.parameters(), lr=1.)
steps = 10
scheduler = optim.lr_scheduler.CosineAnnealingLR(optimizer, steps)

for epoch in range(5):
    for idx in range(steps):
        scheduler.step()
        print(scheduler.get_lr())
    
    print('Reset scheduler')
    scheduler = optim.lr_scheduler.CosineAnnealingLR(optimizer, steps)
