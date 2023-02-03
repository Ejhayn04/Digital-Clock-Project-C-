# Digital-Clock-Project-C-


<h2>Description</h2>
Project consists of a simple C# script that displays a digital clock and allows the user to pick the color and style of their digital clock.
<br />


<h2>Languages and Utilities Used</h2>

- <b>C#</b> 
- <b>.Net Framework</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Digital_Clock
{
    public partial class DigitalClock : Form
    {
        public DigitalClock()
        {
            InitializeComponent();
            //Removing the borders of the colors
            redButton.FlatStyle = FlatStyle.Flat; 
            blueButton.FlatStyle = FlatStyle.Flat;
            darkGreenButton.FlatStyle = FlatStyle.Flat;
            purpleButton.FlatStyle = FlatStyle.Flat;

        }


        private void DigitalClock_Load(object sender, EventArgs e)
        {
            clockTimer.Start(); // Starting the timer
        }

        private void clockTimer_Tick(object sender, EventArgs e)
        {
            clockLabel.Text = DateTime.Now.ToString("hh:mm:ss"); //Programming the timer to display the hour, minute, and seconds.

        }

        private void blueButton_Click(object sender, EventArgs e)
        {
            clockLabel.ForeColor = Color.Blue; // blue button code

        }

        private void purpleButton_Click(object sender, EventArgs e)
        {
            clockLabel.ForeColor = Color.Purple; //purple button code

        }

        private void darkGreenButton_Click(object sender, EventArgs e)
        {
            clockLabel.ForeColor = Color.Yellow; //yellow button code

        }

        private void redButton_Click(object sender, EventArgs e)
        {
            clockLabel.ForeColor = Color.Red; //red button code

        }

        private void styleButton1_Click(object sender, EventArgs e)
        {
            clockLabel.Font = new Font("Lucida Fax",90, FontStyle.Regular); //font style 1 code

        }

        private void styleButton2_Click(object sender, EventArgs e)
        {
            clockLabel.Font = new Font("Noto Serif", 90, FontStyle.Regular); //font style 2 code
        }

        private void styleButton3_Click(object sender, EventArgs e)
        {
            clockLabel.Font = new Font("Open Sans", 90, FontStyle.Regular); // font style 3 code
        }
    }
}


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
