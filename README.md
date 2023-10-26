# snake-agme

###PROGRAM:
```
import pygame 

pygame.init()
screen_width=500
screen_height=400
screen=pygame.display.set_mode((screen_width,screen_height))

green_color=(0,255,0)
x=50
y=100
width=15
height=15
speed=2
dir_x=0
dir_y=0

clock=pygame.time.Clock()
while True:
    for event in pygame.event.get():
        if event.type==pygame.QUIT:
             pygame.quit()
             break
    keys=pygame.key.get_pressed()
    if keys[pygame.K_RIGHT] :
        dir_x=0
        dir_x=dir_x+speed
        dir_y=0
    elif keys[pygame.K_LEFT] :
        dir_x=0
        dir_x=dir_x-speed
        dir_y=0
    elif keys[pygame.K_DOWN] :
        dir_y=0
        dir_y=dir_y+speed
        dir_x=0
    elif keys[pygame.K_UP] :
        dir_y=0
        dir_y=dir_y-speed
        dir_x=0

    x=x+dir_x
    y=y+dir_y
    screen.fill((0,0,0))
    pygame.draw.rect(screen,green_color,(x,y,width,height))
    pygame.display.update()
    clock.tick(60)

```
```
