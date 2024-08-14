<script>
    import Logo from '../assets/Logo.png';
    
   
    const menu = [
        { text: 'Home', url: '/' },
        { text: 'Materi', url: '/materi' },
        { text: 'Quiz', url: '/quiz' },
        { text: 'Blog', url: '/blog' },
        { text: 'Forum', url: '/forum' },
        { text: 'Profile', url: '/profile' },
    ];
    

    let currentUrl = '/'; 
</script>

<nav class="w-full py-3 fixed top-4 ">
    <main class="container flex justify-between items-center">
        <img src={Logo} alt="Logo" class="aspect-auto" draggable="false">
        
        <ul class="flex items-center  text-lg font-semibold bg-[#383F51] bg-opacity-25 rounded-3xl">
            {#each menu as item}
                <li>
                    <a
                        href={item.url}
                        class={`block px-8 py-4 rounded-3xl ${item.url === currentUrl ? 'bg-purple-600 text-white' : 'hover:bg-gray-200'}`}
                    >
                        {item.text}
                    </a>
                </li>
            {/each}
        </ul>
        
        <ul class="flex gap-4 items-center">
            <div class="bg-[#383F51] bg-opacity-25 aspect-square rounded-full h-8"></div>
            <div class="bg-[#383F51] bg-opacity-25 aspect-square rounded-full h-16"></div>
        </ul>
    </main>
</nav>

