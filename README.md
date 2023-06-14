# yousi13

22
32
122
import random    
import time  

# 定义颜色    
BLACK = (0, 0, 0)    
WHITE = (255, 255, 255)    
GREEN = (0, 255, 0)    
RED = (255, 0, 0)

# 初始化 Pygame    
pygame.init()

# 创建窗口大小    
screen_width = 800    
screen_height = 600    
screen = pygame.display.set_mode((screen_width, screen_height))

# 创建时钟对象    
clock = pygame.time.Clock()

# 游戏循环    
while True:    
    # 处理事件    
    for event in pygame.event.get():    
        if event.type == pygame.QUIT:    
            pygame.quit()    
            quit()    
        elif event.type == pygame.KEYDOWN:    
            if event.key == pygame.K_LEFT:    
                pass    
            elif event.key == pygame.K_RIGHT:    
                pass    
            elif event.key == pygame.K_UP:    
                pass    
            elif event.key == pygame.K_DOWN:    
                pass  

    # 随机生成一个 1-100 之间的整数    
    number = random.randint(1, 100)

    # 显示数字    
    pygame.draw.rect(screen, GREEN, (screen_width // 2 - 100, screen_height // 2 - 100, 100, 100))    
    pygame.draw.rect(screen, RED, (screen_width // 2 - 100, screen_height // 2 - 100, 100, 100))    
    screen.fill(WHITE)    
    print(number)

    # 等待一段时间    
    time.sleep(0.5)

    # 更新屏幕    
    pygame.display.update()

    # 控制游戏帧率    
    clock.tick(30)    
