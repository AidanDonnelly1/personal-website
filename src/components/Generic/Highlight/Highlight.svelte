<script>
// @ts-nocheck

    import Step from "../../Step.svelte";
    let steps = [
        {
            name: "CU Robotics",
            icon: "fa-solid fa-robot",
            description:
                "Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.",
        },
        {
            name: "Blueprint Boulder",
            icon: "fa-solid fa-hand-holding-heart",
            description:
                "Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.",
        },
        {
            name: "Work Experience",
            icon: "fa-solid fa-user",
            description:
                "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
        },
    ];
</script>

 <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">       
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                   safas asfasf asf as fsa fas fa sfs a s fas fasfafsf a sfaff as sa sf a sfaff as ss fas fasfafsf a sfaff as sa sf a sfaff as s 
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    as fas as fsa fas fas fasfafsf a sfaff as sa sf a sfaff as s fas fasfafsf a sfaff as sa sf a sfaff as ssa sf a sfaff as sa 
            </Step>
            <Step step={steps[2]}>
                <p>
                    fasasf sa fa sfas fasf a sfaff as sa fa sfas fasf a sfaff as sf a sfaff as sa sf a sfaff as sa 
                </p>
            </Step>
        </div>
    </section>