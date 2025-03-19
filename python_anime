import pygame

# 初期化
pygame.init()

# 画面サイズ
WIDTH, HEIGHT = 800, 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Pygame Animation")

# 色の定義
WHITE = (255, 255, 255)

# 円の設定
x, y = 100, HEIGHT // 2
radius = 30
speed = 5
direction = 1
color = [255, 0, 0]

# メインループ
running = True
clock = pygame.time.Clock()
while running:
    screen.fill(WHITE)
    
    # イベント処理
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    
    # 円の移動
    x += speed * direction
    if x + radius > WIDTH or x - radius < 0:
        direction *= -1  # 反転
    
    # 色を変化させる
    color[0] = (color[0] + 2) % 256
    color[1] = (color[1] + 3) % 256
    color[2] = (color[2] + 5) % 256
    
    # 円を描画
    pygame.draw.circle(screen, color, (x, y), radius)
    
    # 画面更新
    pygame.display.flip()
    clock.tick(60)  # 60FPS

pygame.quit()
