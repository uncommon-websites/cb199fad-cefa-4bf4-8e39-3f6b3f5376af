<script lang="ts">
    import ProductCard from './ProductCard.svelte';

    const features = [
        {
            badge: "Continuous",
            code: "Support",
            title: "Structured Check-ins",
            image: "/generated/image-a-minimalist-illustration-of-a-calendar--1771882524409-0.webp", 
            price: "Weekly"
        },
        {
            badge: "Responsive",
            code: "Care",
            title: "Side-effect Support",
            image: "/generated/image-a-person-holding-a-glass-of-water-and-a--1771882526734-1.webp", 
            price: "24/7"
        },
        {
            badge: "Data-Driven",
            code: "Precision",
            title: "Biomarker Tracking",
            image: "/generated/image-a-close-up-of-a-blood-test-kit-and-a-wea-1771882529337-2.webp",
            price: "Monthly"
        },
        {
            badge: "Clinical",
            code: "Guidance",
            title: "Medical Consults",
            image: "/generated/image-a-person-on-a-video-call-with-a-doctor-o-1771882531533-3.webp",
            price: "On-demand"
        }
    ];
</script>

<section class="bg-gray-900 py-24">
    <div class="container mx-auto px-6 md:px-12">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 text-white">
            <div class="max-w-xl">
                <h2 class="text-4xl md:text-[44px] leading-tight font-medium tracking-tight mb-6">Medication is only the beginning.</h2>
                <p class="text-[17px] text-white/80 font-light max-w-md leading-relaxed">Reset provides the clinical oversight and data-driven insights you need to make GLP-1 therapy work for the long term.</p>
            </div>
            <a href="/" class="hidden md:inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors mt-6 md:mt-0 tracking-wide uppercase">
                View Membership <span class="ml-2">→</span>
            </a>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            {#each features as feature}
                <ProductCard {...feature} isDark={true} />
            {/each}
        </div>

        <div class="mt-12 text-center md:hidden">
            <a href="/" class="inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors text-white tracking-wide uppercase">
                View Membership <span class="ml-2">→</span>
            </a>
        </div>
    </div>
</section>
