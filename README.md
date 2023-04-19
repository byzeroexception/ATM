# ATMpackage help; c import java.awt.Color; import java.awt.Font; import java.awt.event.ActionEvent; import java.awt.event.ActionListener; import java.io.File;

import javax.swing.BorderFactory; import javax.swing.JButton; import javax.swing.JFrame; import javax.swing.JLabel; import javax.swing.JOptionPane; import javax.swing.JPanel; import javax.swing.JPasswordField; import javax.swing.JTextField;

public class ATM { public static JFrame LOGİNMENU = new JFrame(); // public static JFrame PAGENAME = new JFrame(); // public static JFrame PAGENAME2 = new JFrame();

//area A00C2
public static JPanel Page1     = new JPanel();
public static JPanel MainPanel = new JPanel();

//area A00C3
public static JPanel welcomPanel = new JPanel();
public static JLabel LMESSAGE = new JLabel();

//area A00C4
public static JPanel LoginNamePanel = new JPanel();
public static JLabel LNAME = new JLabel();

//area A00C5
public static JPanel LoginPassPanel = new JPanel();
public static JLabel LPASS = new JLabel();

//area A00C6
public static JPanel TextNamePanel = new JPanel();
public static JTextField  LNAME1 = new JTextField(10);

//area A00C7
public static JPanel TextPassPanel = new JPanel();
public static JPasswordField LPASS1 = new JPasswordField(10);

//area A0V4D
public static JButton SUBMİT = new JButton();

/*************************************************************
*  EN        INFO        -------  BİLGİLENDİRME          TR  *
* ---------------------------------------------------------- *
* A00C2  : LoginPage        *   GirişSayfası                 *
* A00C3  : WelcomeText      *   HoşgeldinizYazısı            *
* A00C4  : CustomerNumTxt   *   MüşteriNumarasıYazısı        *
* A00C5  : PasswordTxt      *   ŞifreYazısı                  *
* A00C6  : CustomerNumField *   MüşteriNumaraYazmaAlanı      *
* A00C7  : PasswordField    *   ŞifreYazmaAlanı              *
* PR3LX  : PARABANK_Frame   *   PARABANK_ÇERÇEVE             * 
* BL2KQ  : Frame_CnAddBlok  *   Çerçeve_BirleşenEklemeBloğu  *
* M323IC : MainRunBlok      *   AnaÇalıştırmaBloğu           * 
*                           *                                *
* ************************************************************/






//area A00C2
static void MainPanel() {
	MainPanel.setLayout(null);
	MainPanel.setBackground(Color.DARK_GRAY);
	MainPanel.setBounds(0, 0, 500, 250);
}

//area A00C3
static void welcomPanel() {
	welcomPanel.setBackground(Color.DARK_GRAY);
	welcomPanel.setBounds(70, 20, 350, 50);
}
static void LoginMessage() {
	LMESSAGE.setText("PARABANK'A HOŞGELDİNİZ");
	LMESSAGE.setForeground(Color.white);
	LMESSAGE.setFont(new Font("Serif", Font.PLAIN, 25));
	LMESSAGE.setBounds(140, 10, 500, 30);
	 
}

//area A00C4
static void LoginCustomerPanel() {
	
	LoginNamePanel.setBackground(Color.DARK_GRAY);
	LoginNamePanel.setBounds(25, 100, 200, 30);
	LoginNamePanel.setBorder(BorderFactory.createEmptyBorder(-2, 0, 0, -10));
}
static void LoginCustomerLabel() {
// LoginNamePanel.setBorder(BorderFactory.createEmptyBorder(30, 10, 10, 320)); LNAME.setText("MÜŞTERİ NUMARASI : "); LNAME.setForeground(Color.white); LNAME.setFont(new Font("Serif", Font.PLAIN, 18)); LNAME.setBounds(10, 10, 10,10);

}
//area A00C5 static void LoginPassPanel() { LoginPassPanel.setBackground(Color.DARK_GRAY); LoginPassPanel.setBounds(25, 130, 200, 30); LoginPassPanel.setBorder(BorderFactory.createEmptyBorder(-2, 0, 0,-140)); } static void LoginPasswordLabel() { LPASS.setText("ŞİFRE : "); LPASS.setForeground(Color.white); LPASS.setFont(new Font("Serif", Font.PLAIN, 18)); LPASS.setBounds(10, 10, 10, 10);

}

//area A00C6
static void TextNamePanel() {
	TextNamePanel.setBackground(Color.DARK_GRAY);
	TextNamePanel.setBounds(228, 100, 150, 29);
	TextNamePanel.setBorder(BorderFactory.createEmptyBorder(1, 0, 0,20));	
}
static void TextNameField() {
	LNAME1.setBackground(new Color(90,90,90));
	LNAME1.setForeground(Color.white);
	LNAME1.setBorder(BorderFactory.createEmptyBorder(0,0,0,0));
	LNAME1.setFont(new Font("",Font.PLAIN,16));
}

//area A00C7
static void TextPassPanel() {
	TextPassPanel.setBackground(Color.DARK_GRAY);
	TextPassPanel.setBounds(228, 131, 150, 29);
	TextPassPanel.setBorder(BorderFactory.createEmptyBorder(1, 0, 0, 20));
}
static void TextPassField() {
	LPASS1.setBackground(new Color(90,90,90));
	LPASS1.setForeground(Color.white);
	LPASS1.setBorder(BorderFactory.createEmptyBorder(0,0,0,0));
	LPASS1.setFont(new Font("",Font.PLAIN,16));
}


static void Submit() {
	SUBMİT.setText("➜|");
	SUBMİT.setBackground(new Color(232,232,232));
	SUBMİT.setForeground(Color.DARK_GRAY);
	SUBMİT.setBounds(380, 119, 60, 20);
	SUBMİT.setBorder(BorderFactory.createEmptyBorder(0, 0, 0, 0));
}
static void actionevent() { 
	SUBMİT.addActionListener(new ActionListener() {
		public void actionPerformed(ActionEvent i754L) {
			testIt();
		}
	});
}
static void testIt() {
	String CusNum = LNAME1.getText();
	String Pass   = LPASS1.getText();
	if(CusNum.equals("7523") && Pass.equals("1024")) {
		System.err.println("Sistemden Cikildi : Giris Basarili");
		System.exit(0);
	}
	else {
		JOptionPane.showMessageDialog(null,"Üzgünüz giriş bilgileriniz yanlış","[Sistem][PARABANK]",JOptionPane.YES_OPTION);
	}
}


//area PR3LX
static void LoginMenu() {
	LOGİNMENU.setLayout(null);
	LOGİNMENU.getContentPane().setBackground(Color.black);
	LOGİNMENU.setSize(500,250);
	LOGİNMENU.setLocation(600,350);
	LOGİNMENU.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	LOGİNMENU.setResizable(false);
	LOGİNMENU.setVisible(true);
	
	addBlok();
}

//area BL2KQ
static void addBlok() {
MainPanel.add(welcomPanel);
	welcomPanel.add(LMESSAGE);
		welcomPanel();
			LoginMessage();
			
			MainPanel.add(LoginNamePanel);
				LoginNamePanel.add(LNAME);
					LoginNamePanel.add(LNAME1);
						LoginCustomerPanel();
							LoginCustomerLabel();
			
									MainPanel.add(LoginPassPanel);
										LoginPassPanel.add(LPASS);
											LoginPassPanel();
												LoginPasswordLabel();
													
														MainPanel.add(TextNamePanel);
															TextNamePanel.add(LNAME1);
																TextNamePanel();
																	TextNameField();
																
																	MainPanel.add(TextPassPanel);
																		TextPassPanel.add(LPASS1);
																			TextPassField();
		actionevent();										
																			TextPassPanel();
	MainPanel.add(SUBMİT);
	Submit();
																		
	LOGİNMENU.add(MainPanel);
	MainPanel();
}

//area M323IC
public static void main(String [] args) {
	LoginMenu();
}
}
