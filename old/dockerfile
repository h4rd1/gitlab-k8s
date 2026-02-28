# Используем официальный образ GitLab CE как базовый
FROM gitlab/gitlab-ce:latest

# Устанавливаем дополнительные пакеты (пример: curl, unzip)
# Группируем команды для уменьшения числа слоёв
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        curl \
        unzip \
        vim \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Добавляем кастомный конфиг GitLab (если нужен)
# COPY gitlab.rb /etc/gitlab/gitlab.rb


# Открываем порты (стандартные для GitLab)
EXPOSE 80 443 22


# Запускаем GitLab (команда из базового образа)
CMD ["/assets/wrapper"]
