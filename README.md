# AudioCodeForLater
A quick little audio bit I found for playing audio

```java
public void playSound(String filename) 
{
			    
	try 
	{
		Clip clip = AudioSystem.getClip();
		AudioInputStream inputStream = 
			AudioSystem.getAudioInputStream(new File(filename));
		clip.open(inputStream);
		clip.start(); 
	} 
	catch (Exception e) 
	{
		System.err.println(e.getMessage());
	}
			    
}
```
You should copy the FULL path, I have no idea why it won't take just the filename.
