## Abdinasir Mohamed 
<div align="center">
  <img src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/48904a98-e796-467c-935b-ea9c847236c9" alt="coworking-male-programmer-writing-program-code">
</div>

👋 Hi there! I'm an aspiring SWE & Embedded Systems/Software developer 

I'm a highly motivated and collaborative individual eager to delve into the exciting realms of IoT embedded systems, embedded software, DevOps, and robotics. My journey has equipped me with a diverse skill set in various programming languages and frameworks, allowing me to adapt to new challenges with ease.


### About Me :question:

I am passionate about exploring how technology can be harnessed to create innovative solutions. With a strong foundation in computer science, I have developed a keen interest in:

- 🌐 IoT Embedded Systems
- 💻 Embedded Software Development
- 🤖 Robotics
- 🛠️ Software Engineering
- 🚀 DevOps

I'm always excited to learn new things and take on challenging projects. I believe in continuous learning and improvement, and I am dedicated to staying up-to-date with the latest trends and technologies in the field.

### Skills

Here are some of the programming languages and technologies I am proficient in:

<div style="display: flex; justify-content: space-around;">

<div align="center">
<div style="display: flex; align-items: center; gap: 10px;">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/d091104f-e7d9-4df5-837c-5d2b2b1aa980" alt="Java">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/39026a0d-0636-4ed0-b381-1d2d420a262d" alt="Python">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/08bd2ad0-3c20-40d6-8ffb-f8a5dce0a41d" alt="C++">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/5c464694-9d72-4033-9c24-61caf246e32d" alt="C#">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/f30a694b-e35e-40c8-a62b-c1495786fa4b" alt="TypeScript">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/ff281b74-d7de-497c-88aa-af3225cca97c" alt="HTML & CSS">
    <img width="50" src="https://github.com/Abdinasir03/Abdinasir03/assets/115896606/84505f77-635c-45a1-8b51-c65496ba0bb1" alt="JavaScript">
</div>
</div>

<div>
  
**Currently Learning**
<div align="center">

![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white) 
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white) 
![HCL](https://img.shields.io/badge/HCL-555?style=for-the-badge&logo=hashicorp&logoColor=white) 
![YAML](https://img.shields.io/badge/YAML-000?style=for-the-badge&logo=yaml&logoColor=white) 
</div>

### Certifications

I have earned several certifications that validate my skills and knowledge:

- 🎓 **Google UX Design Certificate**
- 🌐 **CompTIA Network+ Certification N10-008**
- 🎓 **Gymnasium - UX Fundamentals**
- 🔒 **Microsoft 365: Implement Security and Threat Management**

Thank you for visiting my GitHub profile! I look forward to connecting with you.

---

**Let's Connect:**
- 🔗 [LinkedIn](https://www.linkedin.com/in/abdinasir-mohamed-357537254/)
- 🌐 [Website](https://www.yourwebsite.com)
- 🐦 [Twitter](https://twitter.com/yourprofile)

---

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Abdinasir03&theme=dark&show_icons=true" alt="Abdinasir's GitHub stats" />
</div>

<div align="center">
  <a href="https://git.io/streak-stats">
    <img src="https://streak-stats.demolab.com/?user=Abdinasir03&theme=dark&show" alt="GitHub Streak" />
  </a>
</div>

![Profile views](https://komarev.com/ghpvc/?username=Abdinasir03)



every10ms - this function runs every 10ms

This function evaluates whether the system should change state (only occassionally)

The system stays in each state for a number of cycles, counted by the 'count'
variable. Each cycle is 10ms long, so 100 cycles gives 100 x 10ms = 1 sec
*----------------------------------------------------------------------------*/
int state = REDOFF ;  // this variable holds the current state
int count = OFFPERIOD ; // this counter variable to decremented to zero

void every10ms() {
  if (count > 0) count -- ; // decrement the counter

  switch (state) {

    // there is one case for each state
    // each case has the same structure

    case REDOFF:  // the state names are defined in the gpio.h file
      if (count == 0) {    // now time to change state
        setRedLED(ON) ;    // set the LEDs for the new state
        state = REDON ;    // ... the new state
        count = ONPERIOD ; // reset the counter
      }
      break ;

    case REDON:
      if (count == 0) {
        setRedLED(OFF) ;     // set the LEDs for the new state
        state = GREENOFF ;
        count = OFFPERIOD ;
      }
      break ;

    case GREENOFF:
      if (count == 0) {
        setGreenLED(ON) ;    // set the LEDs for the new state
        state = GREENON ;
        count = ONPERIOD ;
      }
      break ;

    case GREENON:
      if (count == 0) {
        setGreenLED(OFF) ;   // set the LEDs for the new state
        state = REDOFF ;
        count = OFFPERIOD ;
      }
      break ;

  }

  Modify	the	program	so	that:
1. The	7	possible	colours	flash	in	sequence	(with	no	gaps)
2. The	three	‘single’	colours	(red,	green,	blue)	are	on	for	2	seconds	while	the	four	
mixtures	(including	white)	are	on	for	1	sec.	The	whole	cycle	should	repeat	after	
10sec	and	continue	for	ever.
3. There	are 7	states	(instead	of	4	states	as	at	present)
4. 




  

