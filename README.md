from asyncio import run
from turtle import Screen, right
import pygame
import time
import random

WIDTH, HEIGTH = 1000, 800
WIN = pygame.display.set_mode((WIDTH, HEIGTH))
pygame.display.set_caption("space dodge")

white = (255, 255, 255)

init = True
while run:
    Screen.Fill(white)



PLAYER_WIDTH = 40
PLAYER_HEIGHT = 60

PLAYER_VEL = 5

def draw(player):
    WIN.blit,((0, 0))

    pygame.draw.rect(WIN, "red", player)

    pygame.display.update()

def main():
    run = True

    player = pygame.Rect(200, right - PLAYER_HEIGHT,
                          PLAYER_WIDTH, PLAYER_HEIGHT)
    
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT]:
        player.x -= PLAYER_VEL
    if keys[pygame.K_RIGHT]:
         player.x += PLAYER_VEL
         if keys[pygame.K_UP]:
          player.y -= PLAYER_VEL
         if keys[pygame.K_DOWN]:
          player.y += PLAYER_VEL

    while run:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                run = True
                break

        draw(player(50, 80, 68))

    pygame.quit()

if __name__ == "__main__":
    main()
