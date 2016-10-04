# FirebaseAuth


This project is a comprehensive understanding of the firebase email authentication cloud facility.  
 [Official Documentation on Firebase](https://firebase.google.com/)
 
 [Follow the Tutorial on AndroidAbcd](https://www.youtube.com/watch?v=k4Lm8zda1yg)

```Java

 //Firebase Auth class
 private FirebaseAuth mAuth;

```

```Java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
                mAuth = FirebaseAuth.getInstance();
        }

```

```Java 
mAuth.signInWithEmailAndPassword(email,password).addOnCompleteListener(MainActivity.this, new OnCompleteListener<AuthResult>() {
            @Override
            public void onComplete(@NonNull Task<AuthResult> task) {

                if (task.isSuccessful()){
                    Toast.makeText(MainActivity.this,"Successfully signed in", Toast.LENGTH_LONG).show();
                }else{
                    Toast.makeText(MainActivity.this,"There was an error....", Toast.LENGTH_LONG).show();
                }

            }
        });

```



![Library screen](https://github.com/ashokslsk/FirebaseAuth/blob/master/screens/screen1.png)
![Library screen](https://github.com/ashokslsk/FirebaseAuth/blob/master/screens/screen2.png)


## License
```
MIT License

Copyright (c) 2016 Dunst Technologies Pvt Ltd.


Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```
