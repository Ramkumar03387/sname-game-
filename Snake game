package com.interview;

import java.util.Random;
import java.util.Scanner;

public class SnakeGame {
	static int w = 40;
	static int h = 20;
	static int x,y,fx,fy,score;
	static int n = 5;
	static boolean gameover; 
	static Random r = new Random();
	public static void setup() {
			
			gameover = false;
			x = w/2;
			y = h/2;
			fx = r.nextInt(w); 
			fy = r.nextInt(h);
			
	}
						//draw method//
	public static void draw() {
		
		for(int i=0;i<w+2;i++) {
			System.out.print("#");
		}
		System.out.println();
		for(int i=0;i<h;i++) {
			for(int j=0;j<=w;j++) {
				if(j==0||j==w)
					System.out.print("#");
				if(i == fy && j == fx)
					System.out.print("f");
				if(i==y&&j==x)
					System.out.print("0");
				else
					System.out.print(" ");
				
				
			}
			System.out.println();
		}
		
		for(int i=0;i<w+2;i++) {
			System.out.print("#");
		}
		
	}
	public static void logic() {
		if(x == fx && y == fy) {
			score++;
		fx = r.nextInt(w); 
		fy = r.nextInt(h);
		}
		if(x+1 > w || x < 0 || y+1 > h || y < 0) {
			System.out.println("GAME OVER");
			gameover = true;
		}
	}
	public static void run1() {
		Scanner sc = new Scanner(System.in);
		String keyinput = sc.nextLine();
		
			switch (keyinput) {
			case "w": {
				
				y--;
				break;
			}
			case "a": {
				
				x--;
				break;
			}
			case "d": {
				
				x++;
				break;
			}
			case "s": {
				
				y++;
				break;
			}
			case "x":{
				if(y<fy) {
					y+=n;
				}
				if(y>fy) {
					y-=n;
				}
				if(x<fx) {
					x+=n;
				}
				if(x>fx) {
					x-=n;
				}
				break;
			}
			
				
				
		}
			
		
	}
	public static void main(String[] args) {
		
		setup();
		
		while(!gameover) {
			draw();
			run1();
			logic();
			System.out.println("your update score: "+score);
			
		}
	}
}
