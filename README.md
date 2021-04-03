# TicTacToe_Java
just another tic tac toe for java

	import java.util.InputMismatchException;
import java.util.Scanner;

public class TaTeTi {

	public static void main(String[] args) {
		boolean b = false;
		showRules();
		char a[][] = new char[5][5];
		fillBoard(a);
		showBoard(a);
		play(a, b);

	}

	static void play(char a[][], boolean b) {
		int c = 0;
		while (c < 4) {
			if (b == false) {
				turn1(a);
				b = checkWinner(a);
				System.out.println("");
			}
			if (b == false) {
				turn2(a);
				b = checkWinner(a);
				System.out.println("");
			}
			c++;
		}
	}

	static void fillBoard(char a[][]) {

		a[0][0] = ' ';
		a[0][1] = '|';
		a[0][2] = ' ';
		a[0][3] = '|';
		a[0][4] = ' ';

		a[1][0] = '-';
		a[1][1] = '+';
		a[1][2] = '-';
		a[1][3] = '+';
		a[1][4] = '-';

		a[2][0] = ' ';
		a[2][1] = '|';
		a[2][2] = ' ';
		a[2][3] = '|';
		a[2][4] = ' ';

		a[3][0] = '-';
		a[3][1] = '+';
		a[3][2] = '-';
		a[3][3] = '+';
		a[3][4] = '-';

		a[4][0] = ' ';
		a[4][1] = '|';
		a[4][2] = ' ';
		a[4][3] = '|';
		a[4][4] = ' ';

	}

	static void showBoard(char a[][]) {
		for (int i = 0; i < 5; i++) {
			for (int j = 0; j < 5; j++) {
				System.out.print(a[i][j] + " ");
			}
			System.out.println(" ");
		}
	}

	static void showRules() {
		System.out.println(
				"******************************************************RULES******************************************************");
		String rules = "Select a player and wait for your turn. Tokens: PLAYER1's = 'X', PLAYER2's = 'O'. \nSelect one number from 1 to 9 to draw your token.";
		System.out.println(rules);
		System.out.println("");
		char a[][] = { { '1', '|', '2', '|', '3' }, { '-', '+', '-', '+', '-' }, { '4', '|', '5', '|', '6' },
				{ '-', '+', '-', '+', '-' }, { '7', '|', '8', '|', '9' } };
		showBoard(a);
		System.out.println("");
		System.out.println(
				"*****************************************************************************************************************");
	}

	static boolean checkWinner(char a[][]) {

		if (a[0][0] == 'X' && a[0][2] == 'X' && a[0][4] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[2][0] == 'X' && a[2][2] == 'X' && a[2][4] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[4][0] == 'X' && a[4][2] == 'X' && a[4][4] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][0] == 'X' && a[2][0] == 'X' && a[4][0] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][2] == 'X' && a[2][2] == 'X' && a[4][2] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][4] == 'X' && a[2][4] == 'X' && a[4][4] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][0] == 'X' && a[2][2] == 'X' && a[4][4] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][4] == 'X' && a[2][2] == 'X' && a[4][0] == 'X') {
			System.out.println("¡PLAYER1 WINS!");
			System.out.println();
			return true;
		} else if (a[0][0] == 'O' && a[0][2] == 'O' && a[0][4] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[2][0] == 'O' && a[2][2] == 'O' && a[2][4] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[4][0] == 'O' && a[4][2] == 'O' && a[4][4] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[0][0] == 'O' && a[2][0] == 'O' && a[4][0] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[0][2] == 'O' && a[2][2] == 'O' && a[4][2] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[0][4] == 'O' && a[2][4] == 'O' && a[4][4] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[0][0] == 'O' && a[2][2] == 'O' && a[4][4] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else if (a[0][4] == 'O' && a[2][2] == 'O' && a[4][0] == 'O') {
			System.out.println("¡PLAYER2 WINS!");
			System.out.println();
			return true;
		} else {
			return false;
		}
	}

	static void turn1(char a[][]) {

		Scanner sn = new Scanner(System.in);
		System.out.println("PLAYER1's turn");
		try {
			int decision = sn.nextInt();
			switch (decision) {
			case 1:
				if (a[0][0] == ' ') {
					a[0][0] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 2:
				if (a[0][2] == ' ') {
					a[0][2] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 3:
				if (a[0][4] == ' ') {
					a[0][4] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 4:
				if (a[2][0] == ' ') {
					a[2][0] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 5:
				if (a[2][2] == ' ') {
					a[2][2] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 6:
				if (a[2][4] == ' ') {
					a[2][4] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 7:
				if (a[4][0] == ' ') {
					a[4][0] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 8:
				if (a[4][2] == ' ') {
					a[4][2] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			case 9:
				if (a[4][4] == ' ') {
					a[4][4] = 'X';
				} else {
					System.out.println("Slot not available, try again");
					turn1(a);
				}
				break;
			default:
				System.out.println("Introduce a number between 1 and 9");
				break;
			}

			showBoard(a);

		} catch (InputMismatchException e) {
			System.out.println("Wrong option. Try again.");
			turn1(a);
		}

	}

	static void turn2(char a[][]) {
		Scanner sn = new Scanner(System.in);
		System.out.println("PLAYER2's turn");
		try {
			int decision = sn.nextInt();
			switch (decision) {
			case 1:
				if (a[0][0] == ' ') {
					a[0][0] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 2:
				if (a[0][2] == ' ') {
					a[0][2] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 3:
				if (a[0][4] == ' ') {
					a[0][4] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 4:
				if (a[2][0] == ' ') {
					a[2][0] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 5:
				if (a[2][2] == ' ') {
					a[2][2] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 6:
				if (a[2][4] == ' ') {
					a[2][4] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 7:
				if (a[4][0] == ' ') {
					a[4][0] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 8:
				if (a[4][2] == ' ') {
					a[4][2] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			case 9:
				if (a[4][4] == ' ') {
					a[4][4] = 'O';
				} else {
					System.out.println("Slot not available, try again");
					turn2(a);
				}
				break;
			default:
				System.out.println("Introduce a number between 1 and 9");
				break;
			}

			showBoard(a);
		} catch (InputMismatchException e) {
			System.out.println("Wrong option. Try again.");
			turn2(a);
		}

	}

}

