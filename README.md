# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.


## Algorithm:
## Step 1:
To open the unity engine.

## Step 2:
Create a new plane and create a cube and give color for the cube.

## Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

## Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

## Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.

## Step 6:
Next Create a another new scene named as page2.

## Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

## Step 8:
Click the Build and run button in the Build settings and run the scene.

## Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

## Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class CubeProg : MonoBehaviour
{
    Rigidbody rb;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
        
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("lavel2");
        }
        
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "Spheretag")
            Destroy(collision.gameObject);
    }
}

```

## Output:
## Scene 1:
![Screenshot (122)](https://user-images.githubusercontent.com/93434149/204128409-9d264825-2a5c-4441-b4ca-bc5911a40543.png)
## After the Ball Hit the cube:
![Screenshot (120)](https://user-images.githubusercontent.com/93434149/204128413-048ae3e8-305e-4fb4-8d8e-efccf6bf8bb6.png)
## Redirected scene 2:
![Screenshot (121)](https://user-images.githubusercontent.com/93434149/204128419-e7f61e7e-121b-455d-9fdf-8d70ef504937.png)

## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
