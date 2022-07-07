<template>
    <header>
        <nav class="navbar navbar-expand-lg navbar-light bg-light d-flex flex-wrap justify-content-between py-3">
            
            <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto text-dark text-decoration-none">
                <i class="bi bi-bootstrap-fill fs-4"></i>
                <span class="fs-4 ms-2 d-inline-block">{{ HeaderTitle }}</span>
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-md-auto mb-2 mb-lg-0">
                    <li class="nav-item"><a href="#" class="nav-link active" aria-current="page">Home</a></li>
                    <li class="nav-item"><a href="#" class="nav-link">About</a></li>
                </ul>
            </div>
            
        </nav>
    </header>
</template>

<script>
    export default {
    name: "AppHeader",
    data() {
        return {
            HeaderTitle: 'Simple header',
        }
    }
    }
</script>
