Almost works

```csharp
using UnityEngine;
using System.Collections;
 
public class StepsBuilder : MonoBehaviour
{
    public int height = 0;
    public int width = 0;
    public GameObject brickPrefab = null;
    public int widthCounter = 0;
    public int heightCounter = 0;
    public GameObject awesomeBrick = null;
 
    // Use this for initialization
    void Start ()
    {
        while (heightCounter < height)
        {
            while (widthCounter < width)
            {
                awesomeBrick = (GameObject)Instantiate(brickPrefab);
                awesomeBrick.transform.position = new Vector3(widthCounter, heightCounter, 0.0f);
 
                widthCounter++;
            }
 
            widthCounter = heightCounter + 1;
 
            heightCounter++;
        }
    }
```