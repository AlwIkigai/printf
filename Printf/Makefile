# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: asyed <marvin@42.fr>                       +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/10/17 12:02:02 by asyed             #+#    #+#              #
#    Updated: 2023/10/17 12:02:05 by asyed            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC 			= cc
CFLAGS 		= -Wall -Wextra -Werror -I.

SRCS 		= ft_putchar.c ft_putstr.c ft_strlen.c ft_putnbr.c\
				ft_putunbr.c ft_puthex.c ft_voidptr.c ft_printf.c
					
OBJS 		= $(SRCS:%.c=%.o)

NAME 		= libftprintf.a

all:		$(NAME)

$(OBJS): %.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

$(NAME): $(OBJS)
	ar rcs $(NAME) $(OBJS)

clean:
			rm -f $(OBJS)

fclean:		clean
			rm -f $(NAME)

re:			fclean all

.PHONY:		all clean fclean re
