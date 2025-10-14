<template>
  <body>
    <div class="carousel-container">
      <ul class="carousel">
        <!-- Основные элементы -->
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-bath-product.svg"
              width="200"
              height="200"
              alt="Средства для ухода"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Средства для ухода</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-bed.svg"
              width="200"
              height="200"
              alt="Лежанки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Лежанки</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-food.svg"
              width="200"
              height="200"
              alt="Корм"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Корм</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-toys-feather.svg"
              width="200"
              height="200"
              alt="Игрушки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Игрушки</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-travel-bag.svg"
              width="200"
              height="200"
              alt="Переноски"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Переноски</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-tree.svg"
              width="200"
              height="200"
              alt="Когтеточки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Когтеточки</h3>
            </a>
          </section>
        </li>

        <!-- Дубликаты для бесконечной прокрутки -->
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-bath-product.svg"
              width="200"
              height="200"
              alt="Средства для ухода"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Средства для ухода</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-bed.svg"
              width="200"
              height="200"
              alt="Лежанки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Лежанки</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-food.svg"
              width="200"
              height="200"
              alt="Корм"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Корм</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-toys-feather.svg"
              width="200"
              height="200"
              alt="Игрушки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Игрушки</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-travel-bag.svg"
              width="200"
              height="200"
              alt="Переноски"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Переноски</h3>
            </a>
          </section>
        </li>
        <li class="carousel__item">
          <section class="card">
            <img
              class="card__image"
              src="images/cat-tree.svg"
              width="200"
              height="200"
              alt="Когтеточки"
            />
            <a class="card__link" href="#">
              <h3 class="card__title">Когтеточки</h3>
            </a>
          </section>
        </li>
      </ul>
    </div>
  </body>
</template>

<style scoped>
.carousel-container {
  width: 100%;
  overflow: hidden;
  padding: 40px 0;
  position: relative;
}

.carousel {
  display: flex;
  gap: 30px;
  width: max-content;
  margin: 0;
  padding: 0;
  list-style: none;

  /* Анимация */
  animation: scrolling 20s linear infinite;
}

.carousel:hover {
  animation-play-state: paused;
}

.carousel__item {
  flex: 0 0 250px;
  border: 10px solid transparent;
  box-sizing: border-box;
}

.card {
  text-align: center;
  background: #f5f5f5;
  border-radius: 10px;
  padding: 15px;
  transition: transform 0.3s ease;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.card:hover {
  transform: translateY(-5px);
}

.card__image {
  width: 200px;
  height: 200px;
  object-fit: contain;
  border-radius: 8px;
}

.card__link {
  text-decoration: none;
  color: inherit;
  display: block;
}

.card__title {
  margin: 15px 0 0 0;
  font-size: 1.2em;
  color: #333;
  font-weight: 600;
}

@keyframes scrolling {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(
      calc(-250px * 6 - 30px * 5)
    ); /* 6 элементов + 5 промежутков */
  }
}

/* Адаптивность */
@media (max-width: 768px) {
  .carousel-container {
    padding: 20px 0;
  }

  .carousel__item {
    flex: 0 0 200px;
  }

  .card__image {
    width: 150px;
    height: 150px;
  }

  @keyframes scrolling {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(calc(-200px * 6 - 30px * 5));
    }
  }
}
</style>
