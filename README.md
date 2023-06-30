Navigate to the extracted JDK directory:

shell

cd <jdk_directory_path>
(jdk1.8.0_371)
Replace <jdk_directory_path> with the path to the extracted JDK directory. For example:

shell

cd ~/Downloads/jdk1.8.0_371

    Move the JDK directory to a desired location. For example, let's move it to /opt:

shell

sudo mv * /opt/jdk1.8.0_371

    Set the JAVA_HOME environment variable. Open the /etc/environment file using a text editor:

shell

sudo nano /etc/environment

    Add the following line at the end of the file, specifying the path to the JDK installation directory:

makefile

JAVA_HOME="/opt/jdk1.8.0_371"

Make sure to adjust the path if you have chosen a different installation directory.

    Save the file and exit the text editor.

    Update the system's Java alternatives:

shell

sudo update-alternatives --install /usr/bin/java java /opt/jdk1.8.0_371/bin/java 1
sudo update-alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_371/bin/javac 1

    Set the default Java version:

shell

sudo update-alternatives --config java

Select the number corresponding to the JDK version you installed (e.g., 1) and press Enter.

    Verify the Java installation:

shell

java -version

You should see the installed Java version information.

At this point, you should have successfully installed the JDK. You can proceed with running Minecraft or any other Java applications that require Java 8.

If you encounter any issues during the installation or have further questions, please let me know. 
