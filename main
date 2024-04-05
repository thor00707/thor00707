import pygame
pygame.init()
screen = pygame.display.set_mode((550, 800))

running = True
class Player(pygame.sprite.Sprite):
    def __init__(self):
        super().__init__()
        self.image = pygame.Surface((50, 50))
        self.image.fill((255, 255, 255))
        self.rect = self.image.get_rect()
        self.rect.x = 50
        self.rect.y = 50

player = Player()

running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT]:
        player.rect.x -= 5
    if keys[pygame.K_RIGHT]:
        player.rect.x += 5
    if keys[pygame.K_UP]:
        player.rect.x += 5
    if keys[pygame.K_DOWN]:
        player.rect.y += 5
screen.fill((0, 0, 0))
all_sprites.draw(screen)
pygame.display.flip()
pygame.quit()

class Enemy(pygame.sprite.Sprite):
  def init(self):
     super().init()
     self.image = pygame.Surface((50, 50))
     self.image.fill((255, 0, 0))
     self.rect = self.image.get_rect()
     self.rect.x = 500
     self.rect.y = 500

player = Player()
enemy = Enemy()

all_sprites = pygame.sprite.Group()
all_sprites.add(player)
all_sprites.add(enemy)

   for event in pygame.event.get():
      if event.type == pygame.QUIT:
         running = False
keys = pygame.key.get_pressed()
if keys[pygame.K_LEFT]:
    player.rect.x -= 5
if keys[pygame.K_RIGHT]:
    player.rect.x += 5
if keys[pygame.K_UP]:
    player.rect.y -= 5
if keys[pygame.K_DOWN]:
    player.rect.y += 5

if pygame.sprite.collide_rect(player, enemy):
    print("Collision!")

screen.fill((0, 0, 0))
all_sprites.draw(screen)
pygame.display.flip()
pygame.quit()




