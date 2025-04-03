<script>
    /**
     * @type {boolean}
     */
    export let showModal; // boolean

    /**
     * @type {HTMLDialogElement}
     */
    let dialog; // HTMLDialogElement

    $: if (dialog && showModal) dialog.showModal();
</script>

<!-- svelte-ignore a11y-click-events-have-key-events a11y-no-noninteractive-element-interactions -->
<dialog
    bind:this={dialog}
    on:close={() => (showModal = false)}
    on:click|self={() => dialog.close()}
    class="rounded-xl bg-stone-200 border-none"
>
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div on:click|stopPropagation>
        <div class="flex items-center justify-center rounded-lg p-12">
            <!-- Author: FormBold Team -->
            <!-- Learn More: https://formbold.com -->
            <div class="mx-auto w-full max-w-[550px]">
                <form action="https://formspree.io/f/mayraqzw" method="POST">
                    <div class="mb-5">
                        <label
                            for="name"
                            class="mb-3 block text-emerald-800 font-bold poppins border-none"
                        >
                            Full Name
                        </label>
                        <input
                            type="text"
                            name="name"
                            id="name"
                            placeholder="Full Name"
                            class="w-full rounded-md border border-stone-300 bg-stone-100 py-3 px-6 text-base font-medium text-emerald-900 outline-none focus:border-emerald-900 focus:shadow-md"
                        />
                    </div>
                    <div class="mb-5">
                        <label
                            for="email"
                            class="mb-3 block text-emerald-800 font-bold poppins border-none"
                        >
                            Email Address
                        </label>
                        <input
                            type="email"
                            name="email"
                            id="email"
                            placeholder="example@domain.com"
                            class="w-full rounded-md border border-stone-300 bg-stone-100 py-3 px-6 text-base font-medium text-emerald-900 outline-none focus:border-emerald-900 focus:shadow-md"
                        />
                    </div>
                    <div class="mb-5">
                        <label
                            for="message"
                            class="mb-3 block text-emerald-800 font-bold poppins border-none"
                        >
                            Message
                        </label>
                        <textarea
                            rows="4"
                            name="message"
                            id="message"
                            placeholder="Type your message"
                            class="w-full resize-none rounded-md border border-stone-300 bg-stone-100 py-3 px-6 text-base font-medium text-emerald-900 outline-none focus:border-emerald-900 focus:shadow-md"
                        ></textarea>
                    </div>
                    <div class="grid grid-cols-1 content-center">
                        <button
                            class="rounded-full bg-emerald-900 py-3 px-8 poppins font-semibold text-white outline-none focus:shadow-emerald-900 hover:shadow-lg hover:bg-emerald-800"
                        >
                            Submit
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</dialog>

<!-- <style>
	dialog {
		max-width: 32em;
		border-radius: 0.2em;
		border: none;
		padding: 0;
	}
	dialog::backdrop {
		background: rgba(0, 0, 0, 0.3);
	}
	dialog > div {
		padding: 1em;
	}
	dialog[open] {
		animation: zoom 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
	}
	@keyframes zoom {
		from {
			transform: scale(0.95);
		}
		to {
			transform: scale(1);
		}
	}
	dialog[open]::backdrop {
		animation: fade 0.2s ease-out;
	}
	@keyframes fade {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}
	button {
		display: block;
	}
</style> -->
