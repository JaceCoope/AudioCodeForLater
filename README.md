# AudioCodeForLater
A quick little audio bit I found for playing audio

```java
public synchronized void playSound(String filename) 
{
		 new Thread(new Runnable() 
     {
			  // The wrapper thread is unnecessary, unless it blocks on the
			  // Clip finishing; see comments.
			    public void run() 
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
			  }).start();
			}
```
You should copy the FULL path, I have no idea why it won't take just the filename.
