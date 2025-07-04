<script setup>
import ExperienceItem from './components/experience-item.vue'
import SkillStack from './components/skill-stack.vue'
import linkedinicon from '@/assets/icons/linkedin.png'
import profilepic from '@/assets/icons/pb.png'
</script>

<template>
  <body>
    <div id="wrapper">
      <div id="layout">
        <div id="sidepanel">
          <img id="profilephoto" :src="profilepic" />
          <h2>Claudio Graf</h2>
          <p id="devdesc">Software Developer</p>
          <p id="devdesc">Donaueschingen, Germany</p>
          <div class="stack-horizontal actionpanel">
            <a href="https://github.com/cgrafbus" target="_blank">
              <img src="https://cdn.simpleicons.org/github/d6d6d6" alt="GitHub Icon" />
            </a>
            <a href="https://www.linkedin.com/in/claudio-graf-80004a290/" target="_blank">
              <img :src="linkedinicon" alt="LinkedIn Icon" />
            </a>
            <a href="mailto:claudio.graf.bus@gmail.com">
              <img src="https://cdn.simpleicons.org/gmail/d6d6d6" alt="Gmail Icon" />
            </a>
          </div>
        </div>
        <div id="contentpanel">
          <h1>About Me</h1>
          <p>
            I'm a software developer specializing in C# and desktop application development. In
            addition to my professional work, I also build personal projects focused on practical
            and maintainable software solutions.
          </p>
          <p>
            My main interest lies in creating applications that are reliable, efficient, and
            genuinely helpful to users. I prioritize writing clean, well-structured code and
            designing solutions that solve real-world problems without unnecessary complexity.
          </p>
          <p>
            I approach software development as both a profession and a continuous learning process.
            Each project brings new challenges that I address with attention to detail and a focus
            on long-term maintainability.
          </p>
          <h3>Skills</h3>
          <SkillStack header="Languages" :items="['C#', 'Java']" background="#211635"> </SkillStack>
          <SkillStack
            header="Frameworks"
            :items="['WPF', 'WinForms', 'AvaloniaUI', 'ASP.Net']"
            background="#2e1a46"
          >
          </SkillStack>
          <SkillStack
            header="Databases"
            :items="['SQL-Server', 'MySQL', 'Oracle']"
            background="#3c2555"
          >
          </SkillStack>
          <SkillStack
            header="Practices"
            :items="['Agile / Scrum', 'Clean Architecture', 'Unit Testing']"
            background="#462c64"
          >
          </SkillStack>
          <SkillStack
            header="Other"
            :items="['Git', 'DevOps', 'CI/CD', 'REST APIs', 'Postman', 'JSON']"
            background="#512f79"
          >
          </SkillStack>
          <h3>Experience</h3>
          <div id="expcontainer">
            <div id="expline"></div>
            <ExperienceItem
              header="Sage GmbH"
              fromdate="September 2023"
              untildate="Today"
              iconsource="sagelogo"
              content="Developing and maintaining Sage Wincarat, an ERP system specialized in plastic production,
              using WinForms, C#, SQL Server and Oracle. Responsibilites include customizing business
              logic, improving legacy code and ensuring system stability for our clients."
            >
            </ExperienceItem>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<style scoped>
@import './assets/base.css';
p {
  opacity: 85%;
  margin-top: 10px;
  margin-bottom: 10px;
}

#layout {
  display: flex;
  width: 100%;
  gap: 2rem;
  flex-direction: row;
}

#profilephoto {
  border-radius: 100%;
  width: 200px;
  height: 200px;
  image-rendering: optimizeQuality;
}

#devdesc {
  opacity: 60%;
  width: 100%;
  margin-left: 15px;
}

#contentpanel {
  overflow-y: auto;
  padding-left: 1rem;
}

#sidepanel {
  display: flex;
  width: 40%;
  margin-top: 0px;
  text-align: center;
  align-items: center;
  flex-direction: column;
  gap: 0px;
}

#layout {
  display: flex;
  width: 100%;
  gap: 8rem;
  flex-direction: row;
}

#wrapper {
  min-height: 100vh;
  margin-left: 5rem;
  margin-right: 5rem;
  margin-top: 2rem;
  margin-bottom: 2rem;
  border-color: var(--border);
  border-width: 2px;
  border-style: solid;
  border-radius: 20px;
  padding: 2rem;
  font-family: sans-serif;
  box-sizing: border-box;
}

.actionpanel {
  margin-top: 10px;
  gap: 30px;
}

.actionpanel img {
  width: 30px;
  height: 30px;
  transition-duration: 0.2s;
  cursor: pointer;
}

.actionpanel img:hover {
  filter: brightness(1.5);
  transform: scale(1.2);
}

#expline {
  width: 15px;
  border-radius: 5px;
  opacity: 50%;
  height: auto;
  margin-left: 0.5rem;
  background: linear-gradient(50deg, var(--accent-dark), var(--accent), var(--accent-light));

  -webkit-animation: GradientAnim 5s ease infinite;
  -moz-animation: GradientAnim 5s ease infinite;
  animation: GradientAnim 5s ease infinite;
}

h1 {
  margin-top: 0px;
  margin-bottom: 10px;
  font-size: xx-large;
}

h2 {
  margin-left: 15px;
  margin-top: 20px;
  margin-bottom: 10px;
}

h3 {
  margin-top: 20px;
  margin-bottom: 10px;
  font-size: x-large;
}

#profilephoto {
  image-rendering: auto !important;
  border-radius: 100%;
  width: 180px;
  height: 180px;
}

#expcontainer {
  display: flex;
  flex-direction: row;
  gap: 20px;
}

@-webkit-keyframes GradientAnim {
  0% {
    background-position: 10% 0%;
  }
  50% {
    background-position: 91% 100%;
  }
  100% {
    background-position: 10% 0%;
  }
}
@-moz-keyframes GradientAnim {
  0% {
    background-position: 10% 0%;
  }
  50% {
    background-position: 91% 100%;
  }
  100% {
    background-position: 10% 0%;
  }
}
@keyframes GradientAnim {
  0% {
    background-position: 10% 0%;
  }
  50% {
    background-position: 91% 100%;
  }
  100% {
    background-position: 10% 0%;
  }
}

@media (max-width: 900px) {
  #layout {
    flex-direction: column;
    margin-left: 0;
    margin-right: 0;
    gap: 2rem;
  }

  #wrapper {
    margin: 2vw;
    padding: 0;
    border-width: 0px;
  }

  #sidepanel {
    width: 100%;
  }
}
</style>
