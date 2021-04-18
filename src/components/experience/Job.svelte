<script>
  export let job;
  export let color;
</script>

<div class="text-white d-flex justify-content-around my-5">
  <div class="col-3">
    <div class="logo" style="--logo-color: {color}">
      <span class="logo-text">L</span>
    </div>
  </div>
  <div class="d-flex col-9">
    <div class="col-6 text-center my-auto">
      <span class="exp-name">
        {job.companyName}
      </span>
      <div>
        {job.startDate} - {job.endDate}
      </div>
    </div>
    <div class="col-6 text-center my-auto">
      <span class="exp-name">
        {job.jobDescription}
      </span>
      {#each job.techs as tech}
        <div>
          <span>{tech}</span>
        </div>
      {/each}
    </div>
  </div>
</div>

<style>
  .logo {
    height: 150px;
    width: 150px;
    background-color: var(--logo-color);
    border-radius: 9999px;
    padding: 10px 60px;
  }
  .logo-text {
    color: #323232;
    font-size: 5em;
  }
  .exp-name {
    font-weight: 500;
    font-size: 1.7em;
  }
</style>
