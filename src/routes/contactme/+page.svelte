<script>
    // @ts-nocheck

    //variable Init
    let count = 0;
    //function to be called on click
    function incrementCount() {
        //incremtent
        count++;
    }
</script>

<!-- <div class="text-center">
    <form action="https://formspree.io/f/mayraqzw" method="POST">
        <label class="violet-400">
            Your email:
            <input type="email" name="email" />
        </label>
        <label>
            Your message:
            <textarea name="message"></textarea>
        </label>
            your other form fields go here -->
<!-- <button type="submit">Send</button>
    </form>
</div> -->

<h2 class="py-12 text-center font-semibold text-4xl sm:text-5xl md:text-6xl">
    Send me a message!
    <br />
</h2>

<div class="max-w flex flex-col justify-center items-center py-8">
    <form
        id="large-input"
        action="https://formspree.io/f/mayraqzw"
        method="POST"
        class="max-w px-2 py-20"
    >

        <div class="max-w flex items-center py-2">
            <label class="w-full border-2 rounded-md border-violet-400">
                <textarea
                    class="w-full appearance-none bg-transparent border-1 w-full text-slate-50 mr-3 py-1 px-2 leading-tight focus:outline-none px"
                    name="message"
                    placeholder="Enter Message"
                >
                </textarea>
            </label>
            <div class="px-6"></div>
            <button
                type="submit"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-500 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="pr-6 relative z-9">Send!</h4>
            </button>
        </div>
    </form>
</div>
