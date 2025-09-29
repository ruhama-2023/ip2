<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heal Mental Therapy Clinic</title>
    //this is my dream  to open clinic for mental health i did not know how to introduce my self in portfolio so built this project 
    <style>
        *{
            margin:0;
            padding:0;
            box-sizing: border-box;
        }
        body{
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #fdfbd4;
            color: #333;
            padding: 20px;
        }
        #header{
            background-color: powderblue;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
       
        #name{
            text-align: center;
            margin: 10px 0;
            color: #333;
        }
        .signup{
            margin-top: 30px;
            padding: 20px;
            background: #fffbe6;
            border-radius: 10px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }
        .signup h1{
            text-align: center;
            margin-bottom: 20px;
        }
        .signup label{
            display: block;
            margin-top: 10px;
            margin-bottom: 5px;
        }
        .signup input, .signup select{
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .signup button{
            display: block;
            width: 100%;
            padding: 10px;
            background: powderblue;
            color: #333;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
        
        }
        .signup button:hover{
            background: #87ceeb;
        }
        footer{
            margin-top: 40px;
            text-align: center;
            color: #555;
        }
        #p1 {
            display: none; 
        }
        #p2 {
            display: none; 
        }
        #p3 {
            display: none; 
        }
        .divi2 {
            display: flex;
            gap: 30px; /* space between the h3 blocks */
            align-items: flex-start;
            margin-bottom: 20px;
        }
        .divi2 h3, .divi2 p {
            margin: 0;
        }
        .divi2 h3 {
            cursor: pointer;
            background: #e0f7fa;
            padding: 10px 20px;
            border-radius: 8px;
            min-width: 200px;
            text-align: center;
            transition: background 0.2s;
        }
        .divi2 h3:hover {
            background: #b2ebf2;
        }
    </style>


<script>
        document.addEventListener('DOMContentLoaded', function () {
            const form = document.querySelector('.signup form');
            form.addEventListener('submit', function (e) {
                
                e.preventDefault();

                
                const firstName = form['First name'].value.trim();
                const fatherName = form['Father name'].value.trim();
                const age = form['Age'].value.trim();
                const email = form['EMAIL'].value.trim();
                const address = form['address'].value;
                const emergencyContactName = form['Emergency contact name'].value.trim();
                const emergencyContactNumber = form['Emergency contact number'].value.trim();

                let errors = [];
                if (!firstName) errors.push("First name is required.");
                if (!fatherName) errors.push("Father's name is required.");
                if (!age || isNaN(age) || age <= 0) errors.push("Valid age is required.");
                if (!email || !email.includes('@')) errors.push("Valid email is required.");
                if (!address) errors.push("Address is required.");
                if (!emergencyContactName) errors.push("Emergency contact name is required.");
                if (!emergencyContactNumber || !/^\d+$/.test(emergencyContactNumber)) errors.push("Valid emergency contact number is required.");

                
                let feedback = document.getElementById('form-feedback');
                if (!feedback) {
                    feedback = document.createElement('div');
                    feedback.id = 'form-feedback';
                    feedback.style.margin = '10px 0';
                    feedback.style.color = 'red';
                    form.prepend(feedback);
                }

                if (errors.length > 0) {
                    feedback.innerHTML = errors.join('<br>');
                } else {
                    feedback.style.color = 'green';
                    feedback.innerHTML = "Thank you for signing up! Your information has been received.";
                    
                    form.reset();
                    
                    alert("Sign-up successful! Welcome to Heal Mental Therapy Clinic.");
                }
            });

           
            const descrip1 = document.getElementById('descrip1');
            const p1 = document.getElementById('p1');
            descrip1.addEventListener('click', function () {
                p1.style.display = 'block';
            });



            const descrip2 = document.getElementById('descrip2');
            const p2 = document.getElementById('p2');
            descrip2.addEventListener('click', function () {
                p2.style.display = 'block';
            });

            const descrip3 = document.getElementById('descrip3');
            const p3 = document.getElementById('p3');
            descrip3.addEventListener('click', function () {
                p3.style.display = 'block';
            });
        });
    </script>
</head>
<body>
    <div class="div1">
        <header id="header">
            <img src="logo1.png" alt="Heal Mental Therapy Clinic Logo" id="clinic-logo"/> 
        </header>
        <h1 id="name"><strong>Heal Mental Therapy Clinic</strong></h1>
        <hr>
    </div>

    <h2 id="moto">HEALING STARTS HERE 🧠</h2>

    <div class="divi2">
        <h3 id="descrip1">What is mental health?</h3>
        <p id="p1">
            Mental health is a broad term that encompasses your emotional, psychological, and social well-being. It's a fundamental part of your overall health, <b>as important as your physical health.</b>
            Your mental health influences how you handle stress, relate to others, and make decisions throughout your life.
            It's more than just the absence of mental illness. While mental health includes the presence of conditions like depression or anxiety, it also refers to a positive state of well-being where you can cope with life's challenges, work productively, and contribute to your community.<br>
            It exists on a continuum. Your mental health can change over time. You might be in a state of good mental well-being one day and feel more distressed or struggle the next, depending on various factors like life experiences, genetics, and your environment.
            <br>
            In essence, mental health is about your ability to live a fulfilling life, build relationships, and navigate the world with resilience and a sense of purpose.
        </p>

        <h3 id="descrip2">What will happen if I go through mental health therapy?</h3>
        <p id="p2">
            Going through mental health therapy can lead to significant changes in your life. Instead of just "fixing" a problem, it's a process of learning to understand yourself better. You'll gain a deeper awareness of your thoughts, feelings, and behaviors, and how they connect to one another. Over time, you'll develop new coping strategies and skills to manage stress, navigate difficult emotions, and handle challenges more effectively. You may also see an improvement in your relationships as you learn to communicate more clearly and set healthier boundaries. Essentially, therapy helps you build resilience and gives you the tools to live a more fulfilling and balanced life.
        </p>

        <h3 id="descrip3">Why should I choose Heal Mental Therapy Clinic?</h3>
        <p id="p3">
            Choose Heal Mental Therapy Clinic <b>because it is the designated beginning of your journey toward well-being</b>.<br>
            The clinic is more than just a place for temporary relief; it's a foundational step. It addresses the common hesitation and fear people feel before seeking help by establishing a safe, non-judgmental starting point. It suggests that no matter how overwhelming or hopeless your situation feels, this clinic is the place where you can find the support needed to begin the process of change.
        </p>
    </div>

    <div class="signup">
        <h1>SIGN-UP FORM</h1>
        <form action="#" method="post">
            <label for="first_name">First name:</label>
            <input id="first_name" type="text" name="first_name" placeholder="First name" required>

            <label for="father_name">Father's name:</label>
            <input id="father_name" type="text" name="father_name" placeholder="Father's name" required>

            <label for="age">Age:</label>
            <input id="age" type="number" name="age" placeholder="Age" min="0" required>

            <label for="email">Email:</label>
            <input id="email" type="email" name="email" placeholder="Email" required>

            <label for="address">Address:</label>
            <select id="address" name="address" required>
                <option value="">Select your region</option>
                <option>Addis Ababa</option>
                <option>Afar</option>
                <option>Amhara</option>
                <option>Tigray</option>
                <option>Benishangule</option>
                <option>Central Ethiopia</option>
                <option>Gambela</option>
                <option>Harari</option>
                <option>Oromia</option>
                <option>Sidama</option>
                <option>South Ethiopia</option>
                <option>South West Ethiopia</option>
                <option>Somali</option>
            </select>

            <label for="emergency_contact_name">Emergency contact name:</label>
            <input id="emergency_contact_name" type="text" name="emergency_contact_name" placeholder="Emergency contact name" required>

            <label for="emergency_contact_number">Emergency contact number:</label>
            <input id="emergency_contact_number" type="tel" name="emergency_contact_number" placeholder="Emergency contact number" required>

            <button type="submit">SIGN-UP</button>
        </form>
    </div>
    <br>
    <footer>
        <p>Phone number: +251911223344</p>
        <p>Email: ruhamaforreal2021@gmail.com</p>
    </footer>

</body>
</html>





