<script>
    const experiences = [
      {
        company: "ReaderVirt",
        position: "Software Engineering Internship",
        period: "December 2023 - Present",
        location: "Remote",
        bullets: [
          "Designed a PostgreSQL database with Drizzle ORM, creating complex queries and tables.",
          "Developed user interfaces with SvelteKit, leveraging Tailwind CSS and DaisyUI to create responsive design.",
          "Managed Kubernetes clusters to provision and maintain over 1,000 virtual machines."
        ]
      },
      {
        company: "University of Colorado Boulder",
        position: "Computer Science Learning Assistant",
        period: "January 2024 - Present",
        location: "Boulder, CO",
        bullets: [
          "Mentored and instructed over 600 students a semester in CU's Intro to Computer Science course.",
          "Cultivated collaborative learning environments through specialized training.",
          "Adopted effective communication methods to address students' needs."
        ]
      },
      {
        company: "Digital Forces",
        position: "IT Technician",
        period: "May 2023 - August 2023",
        location: "Plainfield, IL",
        bullets: [
          "Provided on-site IT support to over a dozen businesses in the construction industry.",
          "Repaired computers, cameras, printers, and other technologies.",
          "Prepared computers and network switches for future installation."
        ]
      },
      {
        company: "Constable",
        position: "Software Engineering Internship",
        period: "August 2022 - May 2023",
        location: "Remote",
        bullets: [
          "Implemented pytest to validate backend functionality and address edge cases.",
          "Utilized React to enhance the user experience through dynamic interfaces."
        ]
      }
    ];
  </script>
  
  <div class="space-y-6 w-full max-w-4xl mx-auto">
    {#each experiences as exp}
      <div class="card card-border bg-slate-950 p-4 w-full rounded-lg">
        <div class="card-body">
          <div class="card-body p-6 pt-2">
            <div class="flex justify-between items-start">
              <div>
                <h2 class="card-title text-primary font-semibold">{exp.company}</h2>
                <p class="text-sm opacity-75">{exp.position}</p>
                <p class="text-xs opacity-50">{exp.location}</p>
              </div>
              <div class="badge badge-primary flex flex-col">
                <div class="flex flex-row justify-end">
                  <h2 class="font-semibold text-primary">{exp.period}</h2>
                </div>
              </div>
            </div>
            
            <div class="mt-4">
              <ul class="list-disc pl-5 space-y-1">
                {#each exp.bullets as bullet}
                  <li class="text-sm">{bullet}</li>
                {/each}
              </ul>
            </div>
          </div>
        </div>
      </div>
    {/each}
  </div>