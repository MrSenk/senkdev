<script>
  import Job from "./Job.svelte";

  let jobs = [
    {
      companyName: "R y C Consultores",
      startDate: "Nov 2020",
      endDate: "Now",
      jobDescription: "Projects Engineer",
      techs: [
        "React-Native",
        "Expo",
        "NodeJS",
        "AWS Lambda",
        "PLSQL",
        "Java",
        "Heroku",
      ],
    },
    {
      companyName: "AndesLabs",
      startDate: "Sep 2020",
      endDate: "Nov 2020",
      jobDescription: "Web Developer",
      techs: ["VueJS", "NodeJS"],
    },
    {
      companyName: "Everis Temuco",
      startDate: "Jun 2020",
      endDate: "Sep 2020",
      jobDescription: "Web Developer",
      techs: ["React-Native", "Expo", "NodeJS"],
    },
    {
      companyName: "JKU Linz, Austria",
      startDate: "Sep 2019",
      endDate: "Dec 2019",
      jobDescription: "Internship",
      techs: ["C#", "Java"],
    },
    {
      companyName: "FSU Jena, Germany",
      startDate: "Nov 2018",
      endDate: "Jan 2019",
      jobDescription: "Internship",
      techs: ["Flutter", "Python"],
    },
  ];
</script>

<div class="px-5 mx-5 mb-5 py-5">
  {#each jobs as job}
    <Job {job} color="red" />
  {/each}
</div>

<style>
</style>
