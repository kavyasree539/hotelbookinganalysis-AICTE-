{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/nagpureyogesh/EDA_capstone_project/blob/main/EDA_Capstone_team_Pirates_.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "xchUYZpvImjv"
      },
      "outputs": [],
      "source": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **Project Name**    - Hotel Booking Analysis\n",
        "\n",
        "\n",
        " "
      ],
      "metadata": {
        "id": "osGdM9G8RHJ9"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##### **Project Type**    - EDA\n",
        "##### **Contribution**    - Team\n",
        "##### **Team Member 1 -**Shubham Lawate\n",
        "##### **Team Member 2 -**Yogesh Suresh Nagpure\n",
        "##### **Team Member 3 -**Ashish Mahure"
      ],
      "metadata": {
        "id": "-eBXR6wySAIi"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **Project Summary**\n",
        "Hotel Booking Analysis project was done by group of 3 members – Shubham Lawate,Ashish Mahure and myself. In this project we got one csv file as an input.\n",
        "We first decided to take up this project solely due to our mutual interest in Hotel Booking.But when I downloaded the project I was shocked to see so many data in csv file.\n",
        "  So to overcome this we decided to distributes our work between us ,first thing we had done in this project is that we have make a rough structure that what we need to do in this project and what will be generally the problems and \n",
        "their solution .Then we started working on it .\n",
        "  First of all, I Downloaded the \"hotel_bookings.csv\" data file from the almabetter project dashboard to my computer, and then I uplaoded the data from my computer to the Google Drive in order to be able to perform data analysis and get insight from this data by fetching data with importing that data to colab and read it with readcsv.\n",
        "I began by importing all the necessary python packages and libraries : I impored Pandas with the alias pd, imported Numpy with the alias np, and imported matplotlib with the alias plt for the data visualization.\n",
        "I inserted the csv data into Padas dataframe and take some quick insight over the data.\n",
        "\n",
        "The various booking information between two hotels: a city hotel and a resort hotel. It includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things - a total of 32 variables, however, during the first part of the data exploration some variables were deemed redundant and eliminated, and a number of new calculated and categorical variables were created.\n",
        "This data set contains a single file which compares various booking information between two hotels: a city hotel and a resort hotel.\n",
        "Includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.\n",
        "The dataset contains a total of 119390 entire.\n",
        "Based on the results of EDA, hotel can plan on targeting the new customers to increase spends and maintain good relations with the existing customers, the above pattern it is observed that city hotel has maximum booking from the month of April to sep but after that after there is fall down in booking. From booking we observed that City hotels account for 2/3s of all bookings, Resort hotels account for 1/3.City hotels account for 2/3s of all bookings, Resort hotels account for 1/3.\n",
        "UK, France, and Portugal booked the most hotel stays worldwide\n"
      ],
 "metadata": {
        "id": "0Iyd9GvJSv6c"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **GitHub Link -**"
      ],
      "metadata": {
        "id": "ayIz3umdS5Za"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **Problem Statement**\n"
      ],
      "metadata": {
        "id": "PJpxKzKVTHLD"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#### **Define Your Business Objective?**"
      ],
      "metadata": {
        "id": "KNif_vkGTR-I"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## <b> Explore and analyze the data to discover results and statistics "
      ],
      "metadata": {
        "id": "GCOX96NcVtCL"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#Import libraris"
      ],
      "metadata": {
        "id": "B_8gng7eV9Ih"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##Here we have imported the required libraries which will helps us to do different operation to fetch data from dataset properly.  "
      ],
      "metadata": {
        "id": "55DTmxyLQGuG"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "import numpy as np\n",
        "import pandas as pd\n",
        "import seaborn as sns\n",
        "import matplotlib.pyplot as plt\n",
        "%matplotlib inline\n",
        "from seaborn.widgets import color_palette\n",
        "import plotly \n",
        "import plotly.express as px\n"
      ],
      "metadata": {
        "id": "AqrhnfLCRRkQ"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "#import database from google drive\n",
        "from google.colab import drive\n",
        "drive.mount('/content/drive')"
      ],
      "metadata": {
        "id": "yx0Z3SRaWC02",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "56409e34-2948-438d-8c80-fcaafd931def"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Mounted at /content/drive\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#file location is set \n",
        "file_location = '/content/drive/MyDrive/EDA Capstone Project/Hotel Bookings.csv'\n"
      ],
      "metadata": {
        "id": "07v1Ni0gOKtj"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "#use pd.read_csv to read the data \n",
        "Hotels_data=pd.read_csv(file_location)"
      ],
      "metadata": {
        "id": "Iastho7twuMD"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "Hotels_data.head()\n",
        "#it will shows the data of first five rows"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 386
        },
        "id": "teff-bF-YtVF",
        "outputId": "47f4b879-1611-43e5-e0c8-a58c0f024054"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "          hotel  is_canceled  lead_time  arrival_date_year arrival_date_month  \\\n",
              "0  Resort Hotel            0        342               2015               July   \n",
              "1  Resort Hotel            0        737               2015               July   \n",
              "2  Resort Hotel            0          7               2015               July   \n",
              "3  Resort Hotel            0         13               2015               July   \n",
              "4  Resort Hotel            0         14               2015               July   \n",
              "\n",
              "   arrival_date_week_number  arrival_date_day_of_month  \\\n",
              "0                        27                          1   \n",
              "1                        27                          1   \n",
              "2                        27                          1   \n",
              "3                        27                          1   \n",
              "4                        27                          1   \n",
              "\n",
              "   stays_in_weekend_nights  stays_in_week_nights  adults  ...  deposit_type  \\\n",
              "0                        0                     0       2  ...    No Deposit   \n",
              "1                        0                     0       2  ...    No Deposit   \n",
              "2                        0                     1       1  ...    No Deposit   \n",
              "3                        0                     1       1  ...    No Deposit   \n",
              "4                        0                     2       2  ...    No Deposit   \n",
              "\n",
              "   agent company days_in_waiting_list customer_type   adr  \\\n",
              "0    NaN     NaN                    0     Transient   0.0   \n",
              "1    NaN     NaN                    0     Transient   0.0   \n",
              "2    NaN     NaN                    0     Transient  75.0   \n",
              "3  304.0     NaN                    0     Transient  75.0   \n",
              "4  240.0     NaN                    0     Transient  98.0   \n",
              "\n",
              "   required_car_parking_spaces  total_of_special_requests  reservation_status  \\\n",
              "0                            0                          0           Check-Out   \n",
              "1                            0                          0           Check-Out   \n",
              "2                            0                          0           Check-Out   \n",
              "3                            0                          0           Check-Out   \n",
              "4                            0                          1           Check-Out   \n",
              "\n",
              "  reservation_status_date  \n",
              "0              2015-07-01  \n",
              "1              2015-07-01  \n",
              "2              2015-07-02  \n",
              "3              2015-07-02  \n",
              "4              2015-07-03  \n",
              "\n",
              "[5 rows x 32 columns]"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-ba156a83-677f-48b7-b60f-6d322a53dce5\">\n",
              "    <div class=\"colab-df-container\">\n",
              "      <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>hotel</th>\n",
              "      <th>is_canceled</th>\n",
              "      <th>lead_time</th>\n",
              "      <th>arrival_date_year</th>\n",
              "      <th>arrival_date_month</th>\n",
              "      <th>arrival_date_week_number</th>\n",
              "      <th>arrival_date_day_of_month</th>\n",
              "      <th>stays_in_weekend_nights</th>\n",
               "      <th>stays_in_week_nights</th>\n",
              "      <th>adults</th>\n",
              "      <th>...</th>\n",
              "      <th>deposit_type</th>\n",
              "      <th>agent</th>\n",
              "      <th>company</th>\n",
              "      <th>days_in_waiting_list</th>\n",
              "      <th>customer_type</th>\n",
              "      <th>adr</th>\n",
              "      <th>required_car_parking_spaces</th>\n",
              "      <th>total_of_special_requests</th>\n",
              "      <th>reservation_status</th>\n",
              "      <th>reservation_status_date</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Resort Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>342</td>\n",
              "      <td>2015</td>\n",
              "      <td>July</td>\n",
              "      <td>27</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>NaN</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>0.0</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2015-07-01</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>Resort Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>737</td>\n",
              "      <td>2015</td>\n",
              "      <td>July</td>\n",
              "      <td>27</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>NaN</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>0.0</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2015-07-01</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Resort Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>7</td>\n",
              "      <td>2015</td>\n",
              "      <td>July</td>\n",
              "      <td>27</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>NaN</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>75.0</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2015-07-02</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Resort Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>13</td>\n",
              "      <td>2015</td>\n",
              "      <td>July</td>\n",
              "      <td>27</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>304.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>75.0</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2015-07-02</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Resort Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>14</td>\n",
              "      <td>2015</td>\n",
              "      <td>July</td>\n",
              "      <td>27</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>240.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>98.0</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2015-07-03</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "<p>5 rows × 32 columns</p>\n",
              "</div>\n",
              "      <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-ba156a83-677f-48b7-b60f-6d322a53dce5')\"\n",
              "              title=\"Convert this dataframe to an interactive table.\"\n",
              "              style=\"display:none;\">\n",
              "        \n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\"viewBox=\"0 0 24 24\"\n",
              "       width=\"24px\">\n",
              "    <path d=\"M0 0h24v24H0V0z\" fill=\"none\"/>\n",
              "    <path d=\"M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z\"/><path d=\"M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z\"/>\n",
              "  </svg>\n",
              "      </button>\n",
              "      \n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      flex-wrap:wrap;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "      <script>\n",
              "        const buttonEl =\n",
              "          document.querySelector('#df-ba156a83-677f-48b7-b60f-6d322a53dce5 button.colab-df-convert');\n",
              "        buttonEl.style.display =\n",
              "          google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "        async function convertToInteractive(key) {\n",
              "          const element = document.querySelector('#df-ba156a83-677f-48b7-b60f-6d322a53dce5');\n",
              "          const dataTable =\n",
              "            await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                     [key], {});\n",
              "          if (!dataTable) return;\n",
              "\n",
              "          const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "            '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "            + ' to learn more about interactive tables.';\n",
              "          element.innerHTML = '';\n",
              "          dataTable['output_type'] = 'display_data';\n",
              "          await google.colab.output.renderOutput(dataTable, element);\n",
              "          const docLink = document.createElement('div');\n",
              "          docLink.innerHTML = docLinkHtml;\n",
              "          element.appendChild(docLink);\n",
              "        }\n",
              "      </script>\n",
              "    </div>\n",
              "  </div>\n",
              "  "
            ]
          },
          "metadata": {},
          "execution_count": 5
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "Hotels_data.tail()\n",
        "##it will shows the data of last five rows"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 386
        },
        "id": "JmcrOIwsZ7yM",
        "outputId": "7a663803-d30d-4d93-e7ae-13d6e929c841"
      },
      "execution_count": null,
       "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "             hotel  is_canceled  lead_time  arrival_date_year  \\\n",
              "119385  City Hotel            0         23               2017   \n",
              "119386  City Hotel            0        102               2017   \n",
              "119387  City Hotel            0         34               2017   \n",
              "119388  City Hotel            0        109               2017   \n",
              "119389  City Hotel            0        205               2017   \n",
              "\n",
              "       arrival_date_month  arrival_date_week_number  \\\n",
              "119385             August                        35   \n",
              "119386             August                        35   \n",
              "119387             August                        35   \n",
              "119388             August                        35   \n",
              "119389             August                        35   \n",
              "\n",
              "        arrival_date_day_of_month  stays_in_weekend_nights  \\\n",
              "119385                         30                        2   \n",
              "119386                         31                        2   \n",
              "119387                         31                        2   \n",
              "119388                         31                        2   \n",
              "119389                         29                        2   \n",
              "\n",
              "        stays_in_week_nights  adults  ...  deposit_type  agent company  \\\n",
              "119385                     5       2  ...    No Deposit  394.0     NaN   \n",
              "119386                     5       3  ...    No Deposit    9.0     NaN   \n",
              "119387                     5       2  ...    No Deposit    9.0     NaN   \n",
              "119388                     5       2  ...    No Deposit   89.0     NaN   \n",
              "119389                     7       2  ...    No Deposit    9.0     NaN   \n",
              "\n",
              "       days_in_waiting_list customer_type     adr  \\\n",
              "119385                    0     Transient   96.14   \n",
              "119386                    0     Transient  225.43   \n",
              "119387                    0     Transient  157.71   \n",
              "119388                    0     Transient  104.40   \n",
              "119389                    0     Transient  151.20   \n",
              "\n",
              "        required_car_parking_spaces  total_of_special_requests  \\\n",
              "119385                            0                          0   \n",
              "119386                            0                          2   \n",
              "119387                            0                          4   \n",
              "119388                            0                          0   \n",
              "119389                            0                          2   \n",
              "\n",
              "        reservation_status reservation_status_date  \n",
              "119385           Check-Out              2017-09-06  \n",
              "119386           Check-Out              2017-09-07  \n",
              "119387           Check-Out              2017-09-07  \n",
              "119388           Check-Out              2017-09-07  \n",
              "119389           Check-Out              2017-09-07  \n",
              "\n",
              "[5 rows x 32 columns]"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-f8ab5d47-6784-47ee-a330-55f63efd8532\">\n",
              "    <div class=\"colab-df-container\">\n",
              "      <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>hotel</th>\n",
              "      <th>is_canceled</th>\n",
              "      <th>lead_time</th>\n",
              "      <th>arrival_date_year</th>\n",
              "      <th>arrival_date_month</th>\n",
              "      <th>arrival_date_week_number</th>\n",
              "      <th>arrival_date_day_of_month</th>\n",
              "      <th>stays_in_weekend_nights</th>\n",
              "      <th>stays_in_week_nights</th>\n",
              "      <th>adults</th>\n",
              "      <th>...</th>\n",
              "      <th>deposit_type</th>\n",
              "      <th>agent</th>\n",
              "      <th>company</th>\n",
              "      <th>days_in_waiting_list</th>\n",
              "      <th>customer_type</th>\n",
              "      <th>adr</th>\n",
              "      <th>required_car_parking_spaces</th>\n",
              "      <th>total_of_special_requests</th>\n",
              "      <th>reservation_status</th>\n",
              "      <th>reservation_status_date</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>119385</th>\n",
              "      <td>City Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>23</td>\n",
              "      <td>2017</td>\n",
              "      <td>August</td>\n",
              "      <td>35</td>\n",
              "      <td>30</td>\n",
              "      <td>2</td>\n",
              "      <td>5</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>394.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>96.14</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2017-09-06</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119386</th>\n",
              "      <td>City Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>102</td>\n",
              "      <td>2017</td>\n",
              "      <td>August</td>\n",
              "      <td>35</td>\n",
              "      <td>31</td>\n",
              "      <td>2</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>9.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>225.43</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2017-09-07</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119387</th>\n",
              "      <td>City Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>34</td>\n",
              "      <td>2017</td>\n",
              "      <td>August</td>\n",
              "      <td>35</td>\n",
              "      <td>31</td>\n",
              "      <td>2</td>\n",
              "      <td>5</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>9.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>157.71</td>\n",
              "      <td>0</td>\n",
              "      <td>4</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2017-09-07</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119388</th>\n",
              "      <td>City Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>109</td>\n",
              "      <td>2017</td>\n",
              "      <td>August</td>\n",
              "      <td>35</td>\n",
              "      <td>31</td>\n",
              "      <td>2</td>\n",
              "      <td>5</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>89.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>104.40</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2017-09-07</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119389</th>\n",
              "      <td>City Hotel</td>\n",
              "      <td>0</td>\n",
              "      <td>205</td>\n",
              "      <td>2017</td>\n",
              "      <td>August</td>\n",
              "      <td>35</td>\n",
              "      <td>29</td>\n",
              "      <td>2</td>\n",
              "      <td>7</td>\n",
              "      <td>2</td>\n",
              "      <td>...</td>\n",
              "      <td>No Deposit</td>\n",
              "      <td>9.0</td>\n",
              "      <td>NaN</td>\n",
              "      <td>0</td>\n",
              "      <td>Transient</td>\n",
              "      <td>151.20</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>Check-Out</td>\n",
              "      <td>2017-09-07</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "<p>5 rows × 32 columns</p>\n",
              "</div>\n",
              "      <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-f8ab5d47-6784-47ee-a330-55f63efd8532')\"\n",
              "              title=\"Convert this dataframe to an interactive table.\"\n",
              "              style=\"display:none;\">\n",
              "        \n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\"viewBox=\"0 0 24 24\"\n",
              "       width=\"24px\">\n",
              "    <path d=\"M0 0h24v24H0V0z\" fill=\"none\"/>\n",
              "    <path d=\"M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z\"/><path d=\"M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z\"/>\n",
              "  </svg>\n",
              "      </button>\n",
              "      \n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      flex-wrap:wrap;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "      <script>\n",
              "        const buttonEl =\n",
              "          document.querySelector('#df-f8ab5d47-6784-47ee-a330-55f63efd8532 button.colab-df-convert');\n",
              "        buttonEl.style.display =\n",
              "          google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "        async function convertToInteractive(key) {\n",
              "          const element = document.querySelector('#df-f8ab5d47-6784-47ee-a330-55f63efd8532');\n",
              "          const dataTable =\n",
              "            await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                     [key], {});\n",
              "          if (!dataTable) return;\n",
              "\n",
              "          const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "            '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "            + ' to learn more about interactive tables.';\n",
              "          element.innerHTML = '';\n",
              "          dataTable['output_type'] = 'display_data';\n",
              "          await google.colab.output.renderOutput(dataTable, element);\n",
              "          const docLink = document.createElement('div');\n",
              "          docLink.innerHTML = docLinkHtml;\n",
              "          element.appendChild(docLink);\n",
              "        }\n",
              "      </script>\n",
              "    </div>\n",
              "  </div>\n",
              "  "
            ]
          },
          "metadata": {},
          "execution_count": 6
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
"#it will gives the information of all the columns,values,etc.\n",
        "Hotels_data.info()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "b95NehaHaexL",
        "outputId": "efbf7855-f276-48b0-f737-120c091dd712"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "<class 'pandas.core.frame.DataFrame'>\n",
            "RangeIndex: 119390 entries, 0 to 119389\n",
            "Data columns (total 32 columns):\n",
            " #   Column                          Non-Null Count   Dtype  \n",
            "---  ------                          --------------   -----  \n",
            " 0   hotel                           119390 non-null  object \n",
            " 1   is_canceled                     119390 non-null  int64  \n",
            " 2   lead_time                       119390 non-null  int64  \n",
            " 3   arrival_date_year               119390 non-null  int64  \n",
            " 4   arrival_date_month              119390 non-null  object \n",
            " 5   arrival_date_week_number        119390 non-null  int64  \n",
            " 6   arrival_date_day_of_month       119390 non-null  int64  \n",
            " 7   stays_in_weekend_nights         119390 non-null  int64  \n",
            " 8   stays_in_week_nights            119390 non-null  int64  \n",
            " 9   adults                          119390 non-null  int64  \n",
            " 10  children                        119386 non-null  float64\n",
            " 11  babies                          119390 non-null  int64  \n",
            " 12  meal                            119390 non-null  object \n",
            " 13  country                         118902 non-null  object \n",
            " 14  market_segment                  119390 non-null  object \n",
            " 15  distribution_channel            119390 non-null  object \n",
            " 16  is_repeated_guest               119390 non-null  int64  \n",
            " 17  previous_cancellations          119390 non-null  int64  \n",
            " 18  previous_bookings_not_canceled  119390 non-null  int64  \n",
            " 19  reserved_room_type              119390 non-null  object \n",
            " 20  assigned_room_type              119390 non-null  object \n",
            " 21  booking_changes                 119390 non-null  int64  \n",
            " 22  deposit_type                    119390 non-null  object \n",
            " 23  agent                           103050 non-null  float64\n",
            " 24  company                         6797 non-null    float64\n",
            " 25  days_in_waiting_list            119390 non-null  int64  \n",
            " 26  customer_type                   119390 non-null  object \n",
            " 27  adr                             119390 non-null  float64\n",
            " 28  required_car_parking_spaces     119390 non-null  int64  \n",
            " 29  total_of_special_requests       119390 non-null  int64  \n",
            " 30  reservation_status              119390 non-null  object \n",
            " 31  reservation_status_date         119390 non-null  object \n",
            "dtypes: float64(4), int64(16), object(12)\n",
            "memory usage: 29.1+ MB\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "Hotels_data.shape"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "vkAILlsvbllE",
        "outputId": "516fb31d-3314-4102-c04b-45b94ef19507"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "(119390, 32)"
            ]
          },
          "metadata": {},
          "execution_count": 8
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "#first copy the data so that original data will remains unchange."
      ],
      "metadata": {
        "id": "GXCuJ8XtSAPY"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels=Hotels_data.copy()"
      ],
      "metadata": {
        "id": "TzxDOldtbz6L"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels.describe()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 364
        },
        "id": "0QbmVQU-lUVD",
        "outputId": "96500793-3b2f-4c19-c194-cb7aac1d6ff3"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "         is_canceled      lead_time  arrival_date_year  \\\n",
              "count  119390.000000  119390.000000      119390.000000   \n",
              "mean        0.370416     104.011416        2016.156554   \n",
              "std         0.482918     106.863097           0.707476   \n",
              "min         0.000000       0.000000        2015.000000   \n",
              "25%         0.000000      18.000000        2016.000000   \n",
              "50%         0.000000      69.000000        2016.000000   \n",
              "75%         1.000000     160.000000        2017.000000   \n",
              "max         1.000000     737.000000        2017.000000   \n",
              "\n",
              "       arrival_date_week_number  arrival_date_day_of_month  \\\n",
              "count             119390.000000              119390.000000   \n",
              "mean                  27.165173                  15.798241   \n",
              "std                   13.605138                   8.780829   \n",
              "min                    1.000000                   1.000000   \n",
              "25%                   16.000000                   8.000000   \n",
              "50%                   28.000000                  16.000000   \n",
              "75%                   38.000000                  23.000000   \n",
              "max                   53.000000                  31.000000   \n",
              "\n",
              "       stays_in_weekend_nights  stays_in_week_nights         adults  \\\n",
              "count            119390.000000         119390.000000  119390.000000   \n",
              "mean                  0.927599              2.500302       1.856403   \n",
              "std                   0.998613              1.908286       0.579261   \n",
              "min                   0.000000              0.000000       0.000000   \n",
              "25%                   0.000000              1.000000       2.000000   \n",
              "50%                   1.000000              2.000000       2.000000   \n",
              "75%                   2.000000              3.000000       2.000000   \n",
              "max                  19.000000             50.000000      55.000000   \n",
              "\n",
              "            children         babies  is_repeated_guest  \\\n",
              "count  119386.000000  119390.000000      119390.000000   \n",
              "mean        0.103890       0.007949           0.031912   \n",
              "std         0.398561       0.097436           0.175767   \n",
              "min         0.000000       0.000000           0.000000   \n",
              "25%         0.000000       0.000000           0.000000   \n",
              "50%         0.000000       0.000000           0.000000   \n",
              "75%         0.000000       0.000000           0.000000   \n",
              "max        10.000000      10.000000           1.000000   \n",
              "\n",
              "       previous_cancellations  previous_bookings_not_canceled  \\\n",
              "count           119390.000000                   119390.000000   \n",
              "mean                 0.087118                        0.137097   \n",
              "std                  0.844336                        1.497437   \n",
              "min                  0.000000                        0.000000   \n",
              "25%                  0.000000                        0.000000   \n",
              "50%                  0.000000                        0.000000   \n",
              "75%                  0.000000                        0.000000   \n",
              "max                 26.000000                       72.000000   \n",
              "\n",
              "       booking_changes          agent      company  days_in_waiting_list  \\\n",
              "count    119390.000000  103050.000000  6797.000000         119390.000000   \n",
              "mean          0.221124      86.693382   189.266735              2.321149   \n",
              "std           0.652306     110.774548   131.655015             17.594721   \n",
              "min           0.000000       1.000000     6.000000              0.000000   \n",
              "25%           0.000000       9.000000    62.000000              0.000000   \n",
              "50%           0.000000      14.000000   179.000000              0.000000   \n",
              "75%           0.000000     229.000000   270.000000              0.000000   \n",
              "max          21.000000     535.000000   543.000000            391.000000   \n",
              "\n",
              "                 adr  required_car_parking_spaces  total_of_special_requests  \n",
              "count  119390.000000                119390.000000              119390.000000  \n",
              "mean      101.831122                     0.062518                   0.571363  \n",
              "std        50.535790                     0.245291                   0.792798  \n",
              "min        -6.380000                     0.000000                   0.000000  \n",
              "25%        69.290000                     0.000000                   0.000000  \n",
              "50%        94.575000                     0.000000                   0.000000  \n",
              "75%       126.000000                     0.000000                   1.000000  \n",
              "max      5400.000000                     8.000000                   5.000000  "
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-f23d56dc-c4bb-463d-beb5-6dd19dc5b993\">\n",
              "    <div class=\"colab-df-container\">\n",
              "      <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>is_canceled</th>\n",
              "      <th>lead_time</th>\n",
              "      <th>arrival_date_year</th>\n",
              "      <th>arrival_date_week_number</th>\n",
              "      <th>arrival_date_day_of_month</th>\n",
              "      <th>stays_in_weekend_nights</th>\n",
              "      <th>stays_in_week_nights</th>\n",
              "      <th>adults</th>\n",
              "      <th>children</th>\n",
              "      <th>babies</th>\n",
              "      <th>is_repeated_guest</th>\n",
              "      <th>previous_cancellations</th>\n",
              "      <th>previous_bookings_not_canceled</th>\n",
              "      <th>booking_changes</th>\n",
              "      <th>agent</th>\n",
              "      <th>company</th>\n",
              "      <th>days_in_waiting_list</th>\n",
              "      <th>adr</th>\n",
              "      <th>required_car_parking_spaces</th>\n",
              "      <th>total_of_special_requests</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>count</th>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119386.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>103050.000000</td>\n",
              "      <td>6797.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "      <td>119390.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>mean</th>\n",
              "      <td>0.370416</td>\n",
              "      <td>104.011416</td>\n",
              "      <td>2016.156554</td>\n",
              "      <td>27.165173</td>\n",
              "      <td>15.798241</td>\n",
              "      <td>0.927599</td>\n",
              "      <td>2.500302</td>\n",
              "      <td>1.856403</td>\n",
              "      <td>0.103890</td>\n",
              "      <td>0.007949</td>\n",
              "      <td>0.031912</td>\n",
              "      <td>0.087118</td>\n",
              "      <td>0.137097</td>\n",
              "      <td>0.221124</td>\n",
              "      <td>86.693382</td>\n",
              "      <td>189.266735</td>\n",
              "      <td>2.321149</td>\n",
              "      <td>101.831122</td>\n",
              "      <td>0.062518</td>\n",
              "      <td>0.571363</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>std</th>\n",
              "      <td>0.482918</td>\n",
              "      <td>106.863097</td>\n",
              "      <td>0.707476</td>\n",
              "      <td>13.605138</td>\n",
              "      <td>8.780829</td>\n",
              "      <td>0.998613</td>\n",
              "      <td>1.908286</td>\n",
              "      <td>0.579261</td>\n",
              "      <td>0.398561</td>\n",
              "      <td>0.097436</td>\n",
              "      <td>0.175767</td>\n",
              "      <td>0.844336</td>\n",
              "      <td>1.497437</td>\n",
              "      <td>0.652306</td>\n",
              "      <td>110.774548</td>\n",
              "      <td>131.655015</td>\n",
              "      <td>17.594721</td>\n",
              "      <td>50.535790</td>\n",
              "      <td>0.245291</td>\n",
              "      <td>0.792798</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>min</th>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>2015.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>6.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>-6.380000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>25%</th>\n",
              "      <td>0.000000</td>\n",
              "      <td>18.000000</td>\n",
              "      <td>2016.000000</td>\n",
              "      <td>16.000000</td>\n",
              "      <td>8.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>2.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>9.000000</td>\n",
              "      <td>62.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>69.290000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "    </tr>\n",
               "    <tr>\n",
              "      <th>50%</th>\n",
              "      <td>0.000000</td>\n",
              "      <td>69.000000</td>\n",
              "      <td>2016.000000</td>\n",
              "      <td>28.000000</td>\n",
              "      <td>16.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>2.000000</td>\n",
              "      <td>2.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>14.000000</td>\n",
              "      <td>179.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>94.575000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>75%</th>\n",
              "      <td>1.000000</td>\n",
              "      <td>160.000000</td>\n",
              "      <td>2017.000000</td>\n",
              "      <td>38.000000</td>\n",
              "      <td>23.000000</td>\n",
              "      <td>2.000000</td>\n",
              "      <td>3.000000</td>\n",
              "      <td>2.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>229.000000</td>\n",
              "      <td>270.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>126.000000</td>\n",
              "      <td>0.000000</td>\n",
              "      <td>1.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>max</th>\n",
              "      <td>1.000000</td>\n",
              "      <td>737.000000</td>\n",
              "      <td>2017.000000</td>\n",
              "      <td>53.000000</td>\n",
              "      <td>31.000000</td>\n",
              "      <td>19.000000</td>\n",
              "      <td>50.000000</td>\n",
              "      <td>55.000000</td>\n",
              "      <td>10.000000</td>\n",
              "      <td>10.000000</td>\n",
              "      <td>1.000000</td>\n",
              "      <td>26.000000</td>\n",
              "      <td>72.000000</td>\n",
              "      <td>21.000000</td>\n",
              "      <td>535.000000</td>\n",
              "      <td>543.000000</td>\n",
              "      <td>391.000000</td>\n",
              "      <td>5400.000000</td>\n",
              "      <td>8.000000</td>\n",
              "      <td>5.000000</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>\n",
              "      <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-f23d56dc-c4bb-463d-beb5-6dd19dc5b993')\"\n",
              "              title=\"Convert this dataframe to an interactive table.\"\n",
              "              style=\"display:none;\">\n",
              "        \n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\"viewBox=\"0 0 24 24\"\n",
              "       width=\"24px\">\n",
              "    <path d=\"M0 0h24v24H0V0z\" fill=\"none\"/>\n",
              "    <path d=\"M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z\"/><path d=\"M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z\"/>\n",
              "  </svg>\n",
              "      </button>\n",
              "      \n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      flex-wrap:wrap;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "      <script>\n",
              "        const buttonEl =\n",
              "          document.querySelector('#df-f23d56dc-c4bb-463d-beb5-6dd19dc5b993 button.colab-df-convert');\n",
              "        buttonEl.style.display =\n",
              "          google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "        async function convertToInteractive(key) {\n",
              "          const element = document.querySelector('#df-f23d56dc-c4bb-463d-beb5-6dd19dc5b993');\n",
              "          const dataTable =\n",
              "            await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                     [key], {});\n",
              "          if (!dataTable) return;\n",
              "\n",
              "          const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "            '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "            + ' to learn more about interactive tables.';\n",
              "          element.innerHTML = '';\n",
              "          dataTable['output_type'] = 'display_data';\n",
              "          await google.colab.output.renderOutput(dataTable, element);\n",
              "          const docLink = document.createElement('div');\n",
              "          docLink.innerHTML = docLinkHtml;\n",
              "          element.appendChild(docLink);\n",
              "        }\n",
              "      </script>\n",
              "    </div>\n",
              "  </div>\n",
              "  "
            ]
          },
          "metadata": {},
          "execution_count": 10
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "#Data prepartion and cleaning"
      ],
      "metadata": {
        "id": "iQqfV_roYbSq"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1. check is there any null value or missing values"
      ],
      "metadata": {
        "id": "P4zVdHlwSNTF"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels.isnull()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 488
        },
        "id": "VhyKInpEeR8b",
        "outputId": "a31611b4-477e-4861-ed03-6cf0a74d9a2e"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "        hotel  is_canceled  lead_time  arrival_date_year  arrival_date_month  \\\n",
              "0       False        False      False              False               False   \n",
              "1       False        False      False              False               False   \n",
              "2       False        False      False              False               False   \n",
              "3       False        False      False              False               False   \n",
              "4       False        False      False              False               False   \n",
              "...       ...          ...        ...                ...                 ...   \n",
              "119385  False        False      False              False               False   \n",
              "119386  False        False      False              False               False   \n",
              "119387  False        False      False              False               False   \n",
              "119388  False        False      False              False               False   \n",
              "119389  False        False      False              False               False   \n",
              "\n",
              "        arrival_date_week_number  arrival_date_day_of_month  \\\n",
              "0                          False                      False   \n",
              "1                          False                      False   \n",
              "2                          False                      False   \n",
              "3                          False                      False   \n",
              "4                          False                      False   \n",
              "...                          ...                        ...   \n",
              "119385                     False                      False   \n",
              "119386                     False                      False   \n",
              "119387                     False                      False   \n",
              "119388                     False                      False   \n",
              "119389                     False                      False   \n",
              "\n",
              "        stays_in_weekend_nights  stays_in_week_nights  adults  ...  \\\n",
              "0                         False                 False   False  ...   \n",
              "1                         False                 False   False  ...   \n",
              "2                         False                 False   False  ...   \n",
              "3                         False                 False   False  ...   \n",
              "4                         False                 False   False  ...   \n",
              "...                         ...                   ...     ...  ...   \n",
              "119385                    False                 False   False  ...   \n",
              "119386                    False                 False   False  ...   \n",
              "119387                    False                 False   False  ...   \n",
              "119388                    False                 False   False  ...   \n",
              "119389                    False                 False   False  ...   \n",
              "\n",
              "        deposit_type  agent  company  days_in_waiting_list  customer_type  \\\n",
              "0              False   True     True                 False          False   \n",
              "1              False   True     True                 False          False   \n",
              "2              False   True     True                 False          False   \n",
              "3              False  False     True                 False          False   \n",
              "4              False  False     True                 False          False   \n",
              "...              ...    ...      ...                   ...            ...   \n",
              "119385         False  False     True                 False          False   \n",
              "119386         False  False     True                 False          False   \n",
              "119387         False  False     True                 False          False   \n",
              "119388         False  False     True                 False          False   \n",
              "119389         False  False     True                 False          False   \n",
              "\n",
              "          adr  required_car_parking_spaces  total_of_special_requests  \\\n",
              "0       False                        False                      False   \n",
              "1       False                        False                      False   \n",
              "2       False                        False                      False   \n",
              "3       False                        False                      False   \n",
              "4       False                        False                      False   \n",
              "...       ...                          ...                        ...   \n",
              "119385  False                        False                      False   \n",
              "119386  False                        False                      False   \n",
              "119387  False                        False                      False   \n",
              "119388  False                        False                      False   \n",
              "119389  False                        False                      False   \n",
              "\n",
              "        reservation_status  reservation_status_date  \n",
              "0                    False                    False  \n",
              "1                    False                    False  \n",
              "2                    False                    False  \n",
              "3                    False                    False  \n",
              "4                    False                    False  \n",
              "...                    ...                      ...  \n",
              "119385               False                    False  \n",
              "119386               False                    False  \n",
              "119387               False                    False  \n",
              "119388               False                    False  \n",
              "119389               False                    False  \n",
              "\n",
              "[119390 rows x 32 columns]"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-99b70b50-c64a-4074-8710-25d4d09c8815\">\n",
              "    <div class=\"colab-df-container\">\n",
              "      <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>hotel</th>\n",
              "      <th>is_canceled</th>\n",
              "      <th>lead_time</th>\n",
              "      <th>arrival_date_year</th>\n",
              "      <th>arrival_date_month</th>\n",
              "      <th>arrival_date_week_number</th>\n",
              "      <th>arrival_date_day_of_month</th>\n",
              "      <th>stays_in_weekend_nights</th>\n",
              "      <th>stays_in_week_nights</th>\n",
              "      <th>adults</th>\n",
              "      <th>...</th>\n",
              "      <th>deposit_type</th>\n",
              "      <th>agent</th>\n",
              "      <th>company</th>\n",
              "      <th>days_in_waiting_list</th>\n",
              "      <th>customer_type</th>\n",
              "      <th>adr</th>\n",
              "      <th>required_car_parking_spaces</th>\n",
              "      <th>total_of_special_requests</th>\n",
              "      <th>reservation_status</th>\n",
              "      <th>reservation_status_date</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>False</td>\n",
               "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>...</th>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "      <td>...</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119385</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119386</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119387</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119388</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>119389</th>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
               "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>...</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>True</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "      <td>False</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "<p>119390 rows × 32 columns</p>\n",
              "</div>\n",
              "      <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-99b70b50-c64a-4074-8710-25d4d09c8815')\"\n",
              "              title=\"Convert this dataframe to an interactive table.\"\n",
              "              style=\"display:none;\">\n",
              "        \n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\"viewBox=\"0 0 24 24\"\n",
              "       width=\"24px\">\n",
              "    <path d=\"M0 0h24v24H0V0z\" fill=\"none\"/>\n",
              "    <path d=\"M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z\"/><path d=\"M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z\"/>\n",
              "  </svg>\n",
              "      </button>\n",
              "      \n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      flex-wrap:wrap;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "      <script>\n",
              "        const buttonEl =\n",
              "          document.querySelector('#df-99b70b50-c64a-4074-8710-25d4d09c8815 button.colab-df-convert');\n",
              "        buttonEl.style.display =\n",
              "          google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "        async function convertToInteractive(key) {\n",
              "          const element = document.querySelector('#df-99b70b50-c64a-4074-8710-25d4d09c8815');\n",
              "          const dataTable =\n",
              "            await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                     [key], {});\n",
              "          if (!dataTable) return;\n",
              "\n",
              "          const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "            '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "            + ' to learn more about interactive tables.';\n",
              "          element.innerHTML = '';\n",
              "          dataTable['output_type'] = 'display_data';\n",
              "          await google.colab.output.renderOutput(dataTable, element);\n",
              "          const docLink = document.createElement('div');\n",
              "          docLink.innerHTML = docLinkHtml;\n",
              "          element.appendChild(docLink);\n",
              "        }\n",
              "      </script>\n",
              "    </div>\n",
              "  </div>\n",
              "  "
            ]
          },
          "metadata": {},
          "execution_count": 11
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#df_Hotels.isnull().sum()\n",
        "# df_Hotels.isnull().sum().sort_values(ascending=True)\n",
        "df_Hotels.isnull().sum().sort_values(ascending=False)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "RF3yHw5lgvQk",
        "outputId": "996fd801-8b1d-4f3a-9870-9bc029db76a1"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "company                           112593\n",
              "agent                              16340\n",
              "country                              488\n",
              "children                               4\n",
              "reserved_room_type                     0\n",
              "assigned_room_type                     0\n",
              "booking_changes                        0\n",
              "deposit_type                           0\n",
              "hotel                                  0\n",
              "previous_cancellations                 0\n",
              "days_in_waiting_list                   0\n",
              "customer_type                          0\n",
              "adr                                    0\n",
              "required_car_parking_spaces            0\n",
              "total_of_special_requests              0\n",
              "reservation_status                     0\n",
              "previous_bookings_not_canceled         0\n",
              "is_repeated_guest                      0\n",
              "is_canceled                            0\n",
              "distribution_channel                   0\n",
              "market_segment                         0\n",
              "meal                                   0\n",
              "babies                                 0\n",
              "adults                                 0\n",
              "stays_in_week_nights                   0\n",
              "stays_in_weekend_nights                0\n",
              "arrival_date_day_of_month              0\n",
              "arrival_date_week_number               0\n",
              "arrival_date_month                     0\n",
              "arrival_date_year                      0\n",
              "lead_time                              0\n",
              "reservation_status_date                0\n",
              "dtype: int64"
            ]
          },
          "metadata": {},
          "execution_count": 12
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1.1 In this dataset we get 112593 null value in 'company' column so we have replaced the null values with 0"
      ],
      "metadata": {
        "id": "hNNxrdHxSxgs"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#replace the null values 0.0 float\n",
        "df_Hotels['company'] = df_Hotels['company'].fillna(0.0)\n",
        "df_Hotels['company'].head(23)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "2hLGd8clg5r7",
        "outputId": "89ed511a-2466-4f1e-d46d-809c71d9e408"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "0       0.0\n",
              "1       0.0\n",
              "2       0.0\n",
              "3       0.0\n",
              "4       0.0\n",
              "5       0.0\n",
              "6       0.0\n",
              "7       0.0\n",
              "8       0.0\n",
              "9       0.0\n",
              "10      0.0\n",
              "11      0.0\n",
              "12      0.0\n",
              "13      0.0\n",
              "14      0.0\n",
              "15      0.0\n",
              "16      0.0\n",
              "17      0.0\n",
              "18    110.0\n",
              "19      0.0\n",
              "20      0.0\n",
              "21      0.0\n",
              "22      0.0\n",
              "Name: company, dtype: float64"
            ]
          },
          "metadata": {},
          "execution_count": 13
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1.2 In the 'agent' column we have also get 16340 so we have replaced it with 0"
      ],
      "metadata": {
        "id": "hTQq2o62TZ4F"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#here also the value replace with 0.0\n",
        "df_Hotels['agent'] = df_Hotels['agent'].fillna(0.0)\n"
      ],
      "metadata": {
        "id": "pObRs0ImjLsk"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1.3 In country we can not set the country values as 0 becuase it contains country codes representing different countries. So instead of replacing it with zero we have replaced it with the mode value in country column. Mode is nothing but just the most repeating value . "
      ],
      "metadata": {
        "id": "GkNj9G2MT90A"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "Hotels_data.country.mode().to_string()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 36
        },
        "id": "7Eo9HdN5kqqc",
        "outputId": "98bb8eda-33e7-438c-9e54-e98c2a283f24"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "'0    PRT'"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "string"
            }
          },
          "metadata": {},
          "execution_count": 15
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "## we use \"inplace =True\" to make permanent change "
      ],
      "metadata": {
        "id": "f-MRIL-EWa2-"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels['country'].fillna(Hotels_data.country.mode().to_string(), inplace=True)\n"
      ],
      "metadata": {
        "id": "GLzM-hZOtpzU"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1.4 Children Column has the count of children then we replaced missing values with mean values"
      ],
      "metadata": {
        "id": "9-sQ2rDRWxWb"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels['children'].fillna(round(Hotels_data.children.mean()), inplace=True)"
      ],
      "metadata": {
        "id": "wDGgsdfvwgY4"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "##1.5 In the data set some rows have zero guests including adults,children and babies  "
      ],
      "metadata": {
        "id": "yQCVMN4uXI_w"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels[(df_Hotels.adults+df_Hotels.babies+df_Hotels.children)==0].shape #here we get 180,32"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "9muxlGlG9mwN",
        "outputId": "887946aa-dec4-48d0-a251-af32f56c94cd"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "(180, 32)"
            ]
          },
          "metadata": {},
          "execution_count": 18
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "\n",
        "Several rows in the dataset contains values that does not make any sense like having no adults, children and babies so we directly deleted it by using drop  "
      ],
      "metadata": {
        "id": "R-JYxEW4Xbho"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "\n",
        "df_Hotels = df_Hotels.drop(df_Hotels[(df_Hotels.adults+df_Hotels.babies+df_Hotels.children)==0].index)\n"
      ],
      "metadata": {
        "id": "xSg4Ag4--_pS"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "##Check the types of datatypes and converting it into int64"
      ],
      "metadata": {
        "id": "x08JOa192hZa"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels.dtypes"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "EVgWdm-lBV7C",
        "outputId": "4d1056a3-cebf-4470-db18-89c9f34bf433"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "hotel                              object\n",
              "is_canceled                         int64\n",
              "lead_time                           int64\n",
              "arrival_date_year                   int64\n",
              "arrival_date_month                 object\n",
              "arrival_date_week_number            int64\n",
              "arrival_date_day_of_month           int64\n",
              "stays_in_weekend_nights             int64\n",
              "stays_in_week_nights                int64\n",
              "adults                              int64\n",
              "children                          float64\n",
              "babies                              int64\n",
              "meal                               object\n",
              "country                            object\n",
              "market_segment                     object\n",
              "distribution_channel               object\n",
              "is_repeated_guest                   int64\n",
              "previous_cancellations              int64\n",
              "previous_bookings_not_canceled      int64\n",
              "reserved_room_type                 object\n",
              "assigned_room_type                 object\n",
              "booking_changes                     int64\n",
              "deposit_type                       object\n",
              "agent                             float64\n",
              "company                           float64\n",
              "days_in_waiting_list                int64\n",
              "customer_type                      object\n",
              "adr                               float64\n",
              "required_car_parking_spaces         int64\n",
              "total_of_special_requests           int64\n",
              "reservation_status                 object\n",
              "reservation_status_date            object\n",
              "dtype: object"
            ]
          },
          "metadata": {},
          "execution_count": 20
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df_Hotels[['children', 'company', 'agent']] = df_Hotels[['children', 'company', 'agent']].astype('int64')\n"
      ],
      "metadata": {
        "id": "-7lgd76HClW-"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "#Exploratory Data Analysis and Visualization\n"
      ],
      "metadata": {
        "id": "WfHmnr_bC8Ze"
      }
    },
    {
      "cell_type": "markdown",
      "source": [],
      "metadata": {
        "id": "j2IE44qAyRo3"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "sns.set_style('darkgrid')\n",
        "plt.rcParams['font.size'] = 10\n",
        "plt.rcParams['figure.figsize'] = (10, 6)\n",
        "plt.rcParams['figure.facecolor']"
      ],
      "metadata": {
        "id": "I0HupNTDyRbl",
        "outputId": "d0a01465-ddc5-42cb-ef45-6da0a74d27c5",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 36
        }
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "'white'"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "string"
            }
          },
          "metadata": {},
          "execution_count": 22
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "#1)Hotels type ratio\n",
        "The database devided into two types of hotels \"city\" hotels and \"Resort\" hotels.\n",
        "The following pie chart visually represents the relative share in percentages of each type of hotel"
      ],
      "metadata": {
        "id": "nJhZVynybw_N"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "sns.set_style(\"whitegrid\")\n",
        "hotels_type = df_Hotels['hotel'].value_counts()\n",
        "hotels_type\n",
        "plot = hotels_type.plot.pie(x = 'City Hotel', y='Resort Hotel', autopct='%1.1f%%', figsize=(5, 5))\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 303
        },
        "id": "JrqPKJcBZbTL",
        "outputId": "0a8a04e1-8419-458a-9b76-26e0efd1866b"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 360x360 with 1 Axes>"
            ],
            "image/png": "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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "The pie chart reveals that 66% of the hotels in the dataset are city hotels and the other 34% are resort hotels.\n",
        "\n"
      ],
      "metadata": {
        "id": "ZV6JPJH-b6io"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##2)which month has maximum arrival in the year ?"
      ],
      "metadata": {
        "id": "qFEdfyVWFn63"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(12,4))\n",
        "sns.countplot(x='arrival_date_month', hue = 'hotel', data= df_Hotels ,palette= ['r','g'])\n",
        "plt.title('Months of Arrival')\n",
        "plt.show()\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 301
        },
        "id": "YiMoBkgfEmsd",
        "outputId": "6032e7f1-72ec-40e7-ac35-8277864ef42f"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 864x288 with 1 Axes>"
            ],
            "image/png": "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Me7fT9FpPY6vfKrM46vMYwM4vnwcX/lUmcdXmccGcHz5KsP4lEpFkSd+y2xqyqJFi3DhwgWsWLECKpUKANCyZUs8ffoUp0+fBgBs3boVnp6eL9VGRERERFQRlMkZ8atXr2L16tV47bXXEBgYCACoV68eVqxYgQULFiAkJETrawgBQKlUlqqNiIiIiKgiKJMg/vrrr+Off/4psK1169aIiorSaxsRERERUXnHX9YkIiIiIpIBgzgRERERkQwYxImIiIiIZMAgTkREREQkAwZxIiIiIiIZMIgTEREREcmAQZyIiIiISAYM4kREREREMmAQJyIiIiKSAYM4EREREZEMGMSJiIiIiGTAIE5EREREJAMGcSIiIiIiGTCIExERERHJgEGciIiIiEgGDOJERERERDJgECciIiIikgGDOBERERGRDBjEiYiIiIhkwCBORERERCQDBnEiIiIiIhkwiBMRERERyYBBnIiIiIhIBgziREREREQyYBAnIiIiIpIBgzgRERERkQwYxImIiIiIZMAgTkREREQkAwZxIiIiIiIZMIgTEREREcmAQZyIiIiISAYM4kREREREMmAQJyIiIiKSAYM4EREREZEMGMSJiIiIiGTAIE5EREREJAMGcSIiIiIiGTCIExERERHJoEIH8evXryMgIADdu3dHQEAAbty4IXdJREREREQ6qdBBPCQkBAMGDMD+/fsxYMAATJ8+Xe6SiIiIiIh0Yix3AaX18OFD/P3331i/fj0AwNvbG7Nnz0ZSUhKsrKx06kOpVLywzMzGWq91PsvGXLe6SqqgcRTGUOMz1NgAju9ZFW185WFsAMdXWuVhfHztlV5lHl95GBvA8ZVWeRhfWb32ihurQgghDFaJAV24cAFTp05FTEyMtMzLywthYWFo0aKFjJURERERERWvQk9NISIiIiKqqCpsELezs0NCQgJyc3MBALm5uUhMTISdnZ3MlRERERERFa/CBnFra2s0a9YM0dHRAIDo6Gg0a9ZM5/nhRERERERyqrBzxAEgNjYWwcHBePLkCSwsLBAaGorGjRvLXRYRERERUbEqdBAnIiIiIqqoKuzUFCIiIiKiioxBnIiIiIhIBgziREREREQyYBAnIiIiIpIBg7geeHh44MqVKy+9jhweP36MVq1aYc6cObJsf/ny5cjKytJ5/X379qFXr17w8/ODp6cnPvnk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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " from the above graph it is observed that Generally, the months of November to March are off-peak periods for hoteliers. Between June and the end of August, attendance is at its peak, it is the high season. Seasonal downturns are experienced by everyone involved in the journey."
      ],
      "metadata": {
        "id": "ppBRL3RF6HxI"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##3)which year has maximum booking ?"
      ],
      "metadata": {
        "id": "bVRTwWJ8GBDl"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Visualizing Hotel wise yearly bookings\n",
        "sns.countplot (x= 'arrival_date_year', data= df_Hotels, hue= 'hotel',palette= ['b','g']).set_title ('yearly bookings')\n"
      ],
      "metadata": {
        "id": "qT7CjuJAONNt",
        "outputId": "5371834f-3a92-4f99-d8ee-dcd7cbc0bad4",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 427
        }
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Text(0.5, 1.0, 'yearly bookings')"
            ]
          },
          "metadata": {},
          "execution_count": 41
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "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tGrVKg0dOlQ7duxQ8+bNi/TVvXt3rVq1yv7622+/VbVq1dSwYUNJ0v3336/169dr27ZtuuuuuzRmzJgS1bp582a99957eu+997RhwwZt27atSHulSpWUkJCglJQUzZs3T4sXL9bGjRslSR999JGkS8+s/emnn9S0aVNt3LhR8+bN05tvvqlt27apefPmGj169DVr6N27t1atWiWr1Srp0oPjt23bpsjISFmtVg0bNkyhoaHavHmz3n//fb3//vvasmWLJMlkMukf//iHvv/+ey1ZskTbtm3Txx9/XKT/jRs36pNPPtGaNWtK9N4AKH2EPABlWteuXVWjRg2ZTCZ169ZNderU0a5duyRJwcHB6tevn7y8vOzP1Wzfvr2aN28uk8kkb2/vIn09+OCD2rRpk3JzcyVJK1euVPfu3e3tjzzyiPz8/GQ2mzVixAj99ttvyszMdLjWtWvX6qGHHlKDBg3k4+Oj4cOHF2lv2bKlQkNDZTKZdOedd6p79+768ccfr9rfkiVL9Mwzz6hevXry8vLS0KFD9euvv15zNK9x48aqXLmyPWCuWbNG99xzj6pXr65ffvlFZ86c0fDhw2U2m3Xbbbfpscceswe2Ro0aqUmTJvLy8lLt2rXVp08fbd++vUj/zzzzjPz9/e3vN4Cyi6t7AZRpy5Yt08KFC+3BJicnRxkZGfL09FTNmjWvWN9isVy1rzp16qhevXr6+uuv9cADD2jTpk1atmyZpEvX782ePVvr1q3TmTNnZDJd+hs4IyNDlStXdqjWkydPqlGjRvbXtWrVKtL+888/a+bMmdq/f78uXryo/Px8denS5ar9paamaurUqUpISLAvs9lsOnHixBV9/6fevXtrxYoVat26tVasWKEnn3xSknTs2DGdPHlS4eHh9nULCwvtrw8ePKjp06dr9+7dys3NVWFhoX2U87Jrvb8AyhZCHoAy69ixY4qJiVFycrKaNm0qT09P9ezZ097u4eFR4j4jIyPt05n169dXnTp1JF0a1fvqq6+0cOFC1a5dW5mZmWrRooVsNpvDfQcHBystLc3+OjU1tUj76NGj1bdvXy1YsEDe3t6aMmWKMjIyrnosFotFQ4cOVY8ePUp0jD169FBkZKR+++03HThwQB06dLD3V7t2bW3YsKHY7V5++WXdddddevXVV+Xn56fk5GStX7++yDo38p4DcA+mawGUWbm5ufLw8FBAQIAk6fPPP7+hL0P8p27dumnr1q1avHixIiMj7cuzs7NlNptVrVo15ebmatasWSXuu0uXLlq6dKn++OMP5ebm6s033yzSnp2drapVq8rb21u7du0qcn1gQECATCaT/vzzT/uyqKgozZ8/337MmZmZWrt27XXrqFmzpu6++26NHTtWnTp1sk+tNm7cWL6+vpo/f74uXLigwsJC7du3zz79nZ2dLV9fX/n6+urAgQNavHhxid8DAGUHIQ9AmVW/fn0NGjRIUVFRuu+++7Rv3z41a9bspvoMDg5WkyZN9NNPP6lbt2725b169VJISIjatm2r7t27q0mTJiXuu127durfv7/69++vjh07qlWrVkXa4+Li9MYbb6hp06ZKSkpS165d7W2VKlXS0KFD9fjjjys8PFw7d+5Ux44d9fTTT2vUqFFq1qyZIiMjtXnzZodq6dWrl/bt21dk5NPT01Nz587Vb7/9pvbt26tVq1aKiYlRVlaWJGn8+PFatWqVmjVrppdeeqnI+wPg1uNhK8lcBADglrB9+3aNHTtWX3/9NVOsQDnFSB4AGMzFixf1wQcf6JFHHiHgAeUYI3kAUAJz587VvHnzrljevHlzLViwoFRqSElJ0eDBg4tt++yzz/Twww/rzjvv1IIFC+Tn51cqNQEoewh5AAAABsR0LQAAgAER8gAAAAyIkAcAAGBAhDwAAAADIuQBAAAYECEPAADAgP4fGt5opKjyzIoAAAAASUVORK5CYII=\n"
          },
          "metadata": {}
             }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " it is observed from the above graph that 2016 were made near about double of booking compared to 2015 and 2017"
      ],
      "metadata": {
        "id": "NFqPkGco7ZX6"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##4)From which country the most guests came?"
      ],
      "metadata": {
        "id": "pcJJTn_qNszR"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#the most guests are coming.\n",
        "sns.barplot (y= list(df_Hotels.country.value_counts().head (10)), x= list(df_Hotels.country.value_counts().head(10).index))"
      ],
      "metadata": {
        "id": "UTZXYeK4OrYh",
        "outputId": "2f3d725e-e44a-41a3-c994-94086c8a16fa",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 394
        }
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "<matplotlib.axes._subplots.AxesSubplot at 0x7fbbdfbdf670>"
            ]
          },
          "metadata": {},
          "execution_count": 42
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "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sLAwjRs3TsXFxdq0aZMuv/xyLViwQF6vV4899phycnJUXFystLQ0LViwQJJCsgYAANBWNBlosbGxGjBggP/jH/3oRzpw4IBKS0sVFRWltLQ0SdKoUaO0efNmSQrJGgAAQFsR1GvQvF6v1q5dK7fbrfLycl122WX+tfj4eHm9XlVVVYVkDQAAoK2IDObOc+bMUceOHTVmzBi9/vrroZrpgiUkRDs9QrPo2rWT0yMAAAAHBBxo+fn5+vzzz7VixQqFh4crKSlJBw4c8K9XVlYqPDxcsbGxIVkLRkXFMXm9Pv/HrTV0vv662ukRAABAiISHhzV6UCmgU5wLFy5UaWmpli1bJpfLJUlKTU1VTU2NPvjgA0nSunXrNHjw4JCtAQAAtBVhPp/P9313+Oyzz5SRkaGePXuqffv2kqQePXpo2bJl2rlzp3Jzc+XxeNS9e3fNnz9fXbp0kaSQrAWqoSNoWY+vDupzOG3NvNEcQQMA4CL2fUfQmgy01ohAAwAA1l3wKU4AAAC0HAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAGAINAADAmEinB8CFi+vsUqQryukxgnKq1qMj39Q6PQYAACYRaBeBSFeU/jlvnNNjBKX/489KItAAAGgIpzgBAACMIdAAAACMIdAAAACMIdAAAACMIdAAAACMIdAAAACMIdAAAACMaTLQ8vPz5Xa7ddVVV2n37t3+2/fu3avMzEylp6crMzNT+/btC+kaAABAW9FkoN16661avXq1unfvfs7tubm5ysrKUnFxsbKyspSTkxPSNQAAgLaiySsJpKWlfee2iooKlZWVaeXKlZKkjIwMzZkzR5WVlfL5fM2+Fh8f32wbRusT0zlKUS6X02MExVNbq6Pf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irZs2WLy92Jqaqr69u2rtWvX6le/+tV5fY7k5GS1b99ee/fu1TXXXNPME56LQGvCmSdrdHS0lixZosjISO3Zs0fDhg3TwYMHFR0drRdffNHpMc/bf/7zHz366KOqqanRzTffrD59+pxzmP69997TpEmTVFxcrA4dOkg6/f/E5/Ppiy++0KJFi+RyuZzcQqO+fbpo165d2rBhg95++219/vnnGjhwoK6//npJp39xvP/++8rPz5d0+rB2QUGB6UD79v4kafny5dq9e7d27NihLVu26LnnntOmTZv8R9W+/XxuDf/yP/tiJ42dQgoLC2vwsY3d3hps3LhRP/vZzxQdHa3+/furvr5eH374oa699lqnRwvaM888o7/97W/au3ev7rnnHiUnJzs90gU5873n8Xg0YcIE/eUvf1FMTMxFdYrz23s7E59ffvmlkpOTdccdd0g6/ZrmoqIirVu3TpI0YsQIFRQUmAw0SXrkkUd033336e677z7vz9FSF2DiFGcTFi9erMLCQq1evVo33XSTpNMFXVhYqO3bt+vqq6/WzJkznR0yCH369NHnn3+uo0ePSpKuuOIKFRYW6t5779WxY8e+c/8BAwbo1KlT+uyzz/y3LV68WMXFxVq4cKGmTZumw4cPt9j8F2r48OHauHGjtmzZot27d2vNmjWSpMLCQp06dUpDhw6V2+3W2rVr9eqrr6qmpsbhiYPXu3dvjR49WitXrlSnTp30/vvv+9caej5b9/HHH+vKK6/83vvExcX5X2x/xpEjR8y9vi4YBQUFevvtt+V2u+V2u1VZWamCggKnxzov2dnZ2rRpkzZu3KiNGzdq27ZtTo/ULKKiovxHdi82397bjTfeqMLCQm3btk1hYWFatGiRJKmkpETV1dW6//775Xa7tXDhQr333ntmX/rTq1cv/fSnP9XKlSvP6/H//e9/5fF4WuT64ATaBXC5XJo5c6befPNNlZWVOT1OQHr27Klbb71VM2bMOOcc+okTJxq8/6effqrjx4+rR48e31m74447dNNNNzV6CtSyrl27avr06XrqqadUU1Oj9evXa9myZSopKVFJSYm2b9+ua665Rps3b3Z61IAdPHhQH374of/jr776SpWVlQ1+7VqLLVu2aO3atU3+wcb111+vN998U1999ZUkqaqqSq+88ooGDhzYEmM2u48++kjV1dV66623/M/JoqIibd68WSdPnnR6vPPWq1cvTZw4UX/+859b7ChEKHm9Xu3YsaNVvFQgWI3tLTo6WrNmzdLatWt16NAhFRQUKCcnx/883bp1q0aOHGn6dbwTJkzQmjVrdPz48aAe9+WXX2r69Om65557FB0dHaLp/g+nOC9Qly5dNHbsWC1dulTLly93epyAzJ07V8uXL9fdd9+tyMhIxcTEKDExUdnZ2fr000/9h7J9Pp98Pp/mzp3b6JGIRx99VCNHjtSDDz6oxMTEFt7JhRk0aJB69eqlVatWqaqqyn+684whQ4aooKBAw4cPd2jC73f2a9Ck038RuGLFCv3vf/9T+/bt5fV69cgjj5j9i6rGTJw40f82G8nJyXrmmWfUr18/7dmz5zuv8UlNTVVeXp6Sk5P1xBNPaPz48aqvr5fP59OYMWP8bw/T2hQUFOiuu+465xRtt27d1KdPH23evDmov0KzJjMzU6tWrdIbb7yh2267TZI0ePBg/147dOig4uJiJ0ds0pnvvbq6Ol155ZX6zW9+ozfeeKPR56d0+o+QbrnlFv/ayJEj9cgjj7T47E1pbG9nu/rqqzV48GAtWbJE77//vhYsWHDO+pAhQzRt2jSNHz/e5MsMLr30Ug0bNkzPP/+8/7ZFixbpmWee8X88Z84cSdKGDRv0j3/8w/82G0OGDNG9997bInOG+S6Gf8YAAABcRDjFCQAAYAyBBgAAYAyBBgAAYAyBBgAAYAyBBgAAYAyBBgAAYAyBBgAAYAyBBgAAYMz/B/LscTbt8GfyAAAAAElFTkSuQmCC\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " from above it is observed that the most guests are came from PRT which the code of Portugal followed by GBR which is nothing but United Kingdom\n"
      ],
      "metadata": {
        "id": "xghOhBTEBl5I"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##5) Most Number of Guest ?"
      ],
      "metadata": {
        "id": "4IwJmCe3UPOh"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "#number of guest\n",
        "number_of_guest= df_Hotels.country.value_counts().head(10).plot (kind= 'bar');\n",
        "for p in number_of_guest.patches:\n",
        "    number_of_guest.annotate(str(p.get_height()), (p.get_x() * 1.005, p.get_height() * 1.005))"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 390
        },
        "id": "bDPxLvahBAqH",
        "outputId": "ba60aa2e-72f2-48da-833c-69bd90fbee70"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " the most number of guest are from Portugal which we have observed from previous graph now from current graph it is observed that the guests are 48483"
      ],
      "metadata": {
        "id": "SZoaSPjjEzNL"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##6) How many booking cancelled ?"
      ],
      "metadata": {
        "id": "vjQerRtLOdao"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Avg of booking cancellations vis a vis bookings.\n",
        "sns.set(style = \"darkgrid\")\n",
        "plt.title(\"Booking Canceled or not by Hotel Type\")\n",
        "ax = sns.countplot(x = 'hotel', hue = 'is_canceled', data = df_Hotels)"
      ],
      "metadata": {
        "id": "zyOSg1e4UktP",
        "outputId": "b2760cd6-4860-40d7-9e1e-5eebbb18cbea",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 410
        }
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAAAnkAAAGJCAYAAAD2cyUlAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nO3de3zP9f//8ft7Z23YwTZzSM75kIwRKjJkNAwxkW9RjknycUqMRjLkTPIhUfmUcmprmhwSJZ8UH8kpcpzZsA1z2On9/v3Rr/elfWzMTu/ttdv1r71fz9fr+Xq83t5eu+/5fL3eL5PFYrEIAAAAhmJn6wIAAABQ8Ah5AAAABkTIAwAAMCBCHgAAgAER8gAAAAyIkAcAAGBAhDygFDp//rzq1q2rjIyMO9ouXLggf39/ZWZm2qCyord37161atWqyLe1tfXr1+u5556zdRl5UpJrB4oSIQ8oxgIDA9WwYUP5+/uradOmGjRokOLi4gp1n5UqVdL+/ftlb29fKP0fPHhQAwcOVEBAgJo1a6Znn31W69atK5R9lWZ169bVmTNnimRf/fr10+eff55l2f0E4IULF2r06NH5rmPfvn3y9/eXv7+/GjVqpLp161pf+/v768KFC/neB1CSEPKAYm7p0qXav3+/du/eLS8vL02dOtXWJeXZ/v379cILL6hp06basmWL9u7dqylTpui7776zdWk2ZbFYZDabbV1GiRcQEKD9+/dr//79ioqKkiT99NNP1mWVKlWycYVA0SLkASWEs7OzgoKCdPLkSeuy69eva+zYsWrevLnatGmjJUuWWMOC2WzWkiVL1KZNG7Vo0UJjx47V9evXs+07JiZGgYGBOn78+B1Tuf369dO8efPUu3dv+fv7a8CAAUpMTLRuu3HjRrVp00aPPfaYFi9erMDAQP3www/Z7mfmzJkKCQnRoEGD5OnpKZPJpAYNGmj+/PmSpKtXr2rw4MFq3ry5mjZtqsGDB+vixYvW7e9Vy759+9S7d28FBASodevWWr9+vSQpLS1NEREReuqpp9SyZUuFhYXp9u3b2dYYHx+vV199Vc2bN1dgYKBWr15tbbt9+7bGjx+vpk2bqlOnTvr1119z/geT9Msvv6hHjx5q0qSJevTooV9++SXLscydO1e9e/fWo48+qnPnzt2xfWBgoFasWKHOnTurSZMmGjlypFJTU63ta9euVfv27dWsWTMNGTJE8fHxkqS+fftKkrp27Sp/f39FR0dnW5/FYlF4eLiaNGmioKAg7dmzR5K0efNmde/ePcu6K1eu1NChQ+96vHcTHx+vIUOGqFmzZmrfvr3Wrl0rSfruu+/0/vvva/PmzfL391eXLl0k/fnZnjBhgp544gk9+eSTmjt3bp4vITh48KBatmyZZfstW7ZY97Vw4UKNGDFCI0eOlL+/v7p166ajR49mqT2nzwRQnBHygBLi1q1bio6O1qOPPmpdNnXqVF2/fl1bt27VRx99pE2bNlmnPtevX68NGzZo9erV2rp1q27evKnw8PA7+l23bp1mz56tlStXqk6dOtnuOyoqSu+884727Nmj9PR0ffDBB5KkEydO6K233tKsWbO0a9cupaSkWINGdvUfOHBAHTp0yPEYzWazunfvrh07dmjHjh1ydna+o+acaomNjdXAgQP1/PPPa8+ePdq4caPq1asnSZo9e7ZOnTqljRs3asuWLUpISNDixYuz3f/QoUNVt25dfffdd1q1apVWrVqlXbt2SZIWLVqks2fP6ptvvtGKFSu0cePGHI8lOTlZgwcPVr9+/bR37171799fgwcPVlJSknWdTZs2aerUqfrll19yHGXavHmzli9frm3btunYsWPW4Lpnzx69++67mjdvnnbv3q3KlStr1KhRkqRPPvnE2v/+/fvVqVOnbPs+ePCgHnzwQf34448aMWKEhg8fruTkZLVt21bnz5/P8gfFpk2bFBISkuPx3suoUaNUsWJF7dq1SwsWLNCcOXO0Z88etWrVSoMHD1bHjh21f/9+ffnll5Kk8ePHy8HBQVu2bNHGjRv1/fff3zElnFsNGzaUu7u7du/enePxbNu2TUFBQfrPf/6j4OBgDRs2TOnp6ff8TADFGSEPKOZeeeUVBQQEKCAgQN9//71eeuklSVJmZqaio6P1z3/+U25ubqpSpYr69+9v/SUZGRmpF198UVWrVpWrq6tGjRql6OjoLDdbrFq1SitWrNBHH32katWq5VhD9+7dVb16dbm4uCgoKEhHjhyRJH399ddq06aNAgIC5OTkpBEjRshkMmXbx7Vr12Q2m+Xt7Z3jfjw8PNShQweVKVNGbm5uGjp0qH766adc1RIVFaWWLVsqODhYjo6O8vDwUL169WSxWLR27VpN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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "in this plot blue shaded area represents booking not cancelled and orange shaded area represents cancelled and it is observed that more than 30000 booking were cancelled in city hotel followed by more than 10000 in resort hotel"
      ],
      "metadata": {
        "id": "yXJIqFa05JVS"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##7) monthly cancellations"
      ],
      "metadata": {
        "id": "QIlBzqRGUVzA"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Plotting monthly cancellations and customer type\n",
        "a = df_Hotels.groupby(\"customer_type\")['is_canceled'].describe()\n",
        "\n",
        "sns.barplot(x=a.index, y=a[\"mean\"] * 100)"
      ],
      "metadata": {
        "id": "uei9L9srWxlb",
        "outputId": "148778aa-069d-4da4-9c3d-1b75e073b3cb",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 411
        }
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "<matplotlib.axes._subplots.AxesSubplot at 0x7fbbdf94cd90>"
            ]
          },
          "metadata": {},
          "execution_count": 46
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "##8)market segment wise booking"
      ],
      "metadata": {
        "id": "-n1vOBokU0AP"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "plt.title(\"Segments wise booking\")\n",
        "ax = sns.countplot(x = \"market_segment\", data = df_Hotels)\n",
        "plt.xticks(rotation = 90)\n",
        "plt.show()"
      ],
      "metadata": {
        "id": "XmUSMGbnX5MF",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 489
        },
        "outputId": "59c37d75-41ae-4fff-f437-b33335992844"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 720x432 with 1 Axes>"
            ],
            "image/png": "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48dr3rx56tu3rypVqqTBgwerb9++On36tPbt2+cqfZKUm5urHj165JtTkvz9/V1/r1Gjhux2u86fP6+UlBTVqFHDdc7Ly0v+/v46e/asfHx8VL169TzZatSoobNnz7o+TkhIUNmyZRUeHl7gY0sFP69paWm6fPlynnzX/h3ArUfJA1Bk6tWrp7CwMK1YsULSlX/UIyIi8i0px48fz1MqnE6nfvnllz/1uLfddptKly6tTz75JN8i9kfyG4bs3r27unfvrszMTEVFRWnOnDmKiYm57vOaN2+u2bNnq3r16mrevLmaNWumadOmydfXV82bN8/38apWreoaVt29e7cGDx6s5s2by9/fX82bN9fSpUsLnT05OTnP30uVKqXbbrtNd9xxhw4dOuQ653Q6lZycrGrVqsnb21u//PKLHA6Hq+glJyerTp06rs/v16+f0tPTNXz4cC1evFhly5YtdCZJqly5snx8fPTLL78oICDguqwAbj2GawHcMomJiXr33Xdd5Sw5OVnx8fF64IEHJEnh4eFatGiRDh8+LEnKyMjQp59+Kklq166dfv75Z23ZskWXL1/WsmXLXMO8N8vLy0v9+vXTrFmzlJqaKkk6e/asduzYUaivr1Klik6dOuX6+OjRo9q5c6dsNpusVqt8fX3zvSInSXXq1JGvr68+/vhjtWjRQuXLl1eVKlW0adOmAkvep59+6nrOKlWqJIvFIi8vLz388MM6duyY1q5dK7vdLrvdrn379uVZMPF7H3/8sY4cOaKsrCzNmzdPnTp1kre3t7p06aKEhATt3LlTdrtd7777rqxWq5o0aaL7779fpUuX1uLFi2W327Vr1y5t27ZNoaGheb53VFSUAgICFBER4VrEUlje3t7q2LGj3nrrLWVlZSkxMVHr1q27qe8B4OZQ8gDcMuXLl9fevXvVr18/BQYG6tFHH1XDhg0VGRkpSerYsaOGDh2qMWPGqGnTpurWrZu2b98u6cqVnnnz5ikmJkYtW7bUkSNH1LhxY5UqVepPZRk/frxq166tRx99VE2bNtVTTz1V4Jy73+vbt6+OHDmioKAgjRgxQjabTa+99ppatmyp4OBgpaWlacyYMQV+fYsWLeTn5+cajmzRooWcTqfuu+++fD9///796tevn5o0aaJnn31WkydPdi3iWLJkiTZs2KA2bdooODhYc+bMkc1mK/Cx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DFBoaKjKlCmj9u3be+TwEgqvZ8+eWrdu3R8e8xRXFxLcc889slgseW4TaLFY9OOPPxqYzlgbNmxQdHS00tPTdccdd+jEiRO65557WHiBwnn//fc1aNAgRUdH57u/lyfvwH7y5EmNHTtWP/74oywWi+69917FxMTozjvvNDqaYb7//nvFxMTo5MmTys3NldPplMVicfsl/UUlISFBO3bs0OrVqzV79mw98sgjed5te7qjR4+6hvcvX77sOu7JUx6kK6v3U1NTVaVKFUlX7oHscDgMTmWc119/XZL0008/GZzE/cTGxmrNmjUaMmSI1q5dq6+++kqbNm0yOtYNUfLcyNVJ8+XKlTM4ifuJiorSo48+qj59+ki6MjciKipKS5cuNTiZcSZPnqwRI0YoMDBQXl5eRscxnMVicd1y6Pz581q3bp0OHjyokJAQdevWTWPGjDE6oqHGjBmjzp07KywszOOHaK81ZMgQ9erVSw8//LCkK28Wxo4da2woA40dO1Zr1qzRoEGD9P777xsdx634+PioSpUqys3NlXRl/uacOXMMTnVjlDw3Eh4ern379unw4cM6cuSILBaLGjRooMGDB3v8qtK0tDT17dvX9XGfPn30wQcfGJjIeKVLl1b37t2NjuE2wsLCXMMmt912m5566ik99dRT2rdvn9asWWNwOuM5HA5FREQYHcPttG/fXvfdd5927dol6crG6w0aNDA4lXGys7O1adMmnT59Os92IVd58lZWVqtVTqdTtWvX1ocffqiaNWu6phC5K0qeG9mzZ4+GDx+uAQMGqHv37nI6ndq/f7+GDh2qd955Rw888IDREQ3j5eWlo0ePqm7dupKkpKQkj78a0bZtWyUkJHj0L91rFTS9+P777/f4N0mSFBgYqJ9++kn33HOP0VHchtPpVP/+/bVhwwaPLnbXGjNmjFasWKHU1NQ824VI/7ta7qlGjx6tzMxMjRs3TtOnT1dGRoamTZtmdKwbYuGFG3nuuefUq1ev6zbi3LJli9asWaMFCxYYlMx427dv18SJE9WoUSM5nU79/PPPmj17toKDg42OZphWrVrpwoULKleunOsdpifPyQsNDdWbb75ZYNnzxE1cr9WrVy8dOXJEAQEBefZT9PQ5eUOGDNHrr7+uSpUqGR3Frbz66qv6xz/+YXQM/EWUPDfSqVOnAidx3uicp0hLS9PevXslSQ888IDH72N1+vTpfI976r0mGzdurGrVquVb8jx1E9drsQ1R/kaPHq39+/erbdu2eVbte/JCt6uSkpKUmJioDh066OLFi7Lb7fLz8zM6VrH79NNP1aVLFy1btizf848//ngxJyo8hmvdyI1uoO7pN1fH9Ty1zBWkfv36rl36cb2rZS4tLc3j3yBdq0GDBgzV5iMuLk5vv/227Ha7OnTooLNnz2rGjBkeeeeYw4cPq0uXLjpw4IDRUW4aJc+N2O12JSYm5nslwm63G5DIfWzevFlTp05V48aN5XQ6NWnSJM2cOVMdOnQwOlqxGz9+vGJiYtSnT598t9rx9OE35G/v3r164YUX5HA4lJCQoP379+ujjz7SzJkzjY5miMTERCUlJblua/bKK68oMzNT0pXFF57u/fff1+rVq11XqerWratz584ZnMoYzz//vKQrQ9glDSXPjWRnZ2vYsGH5nsvvH3NPMnfuXC1fvtx1k/ljx47p2Wef9ciSN2jQIEnSxIkTDU7iXpo2bWp0BLf26quv6p133tG4ceMkSX/729/c/r6bRemNN97Ic4uq7du368knn9SlS5e0aNEizZ0718B0xitVqtR123l5+mK3Dh06qE+fPurdu7eqV69udJxCoeS5EU+//dKN+Pr6ugqeJNWpU8djh7AbN24siblUv3ftLbtwPbvdft3ik1KlShmUxnjHjx/Ps1K0TJkyrqtW7jzHqrj4+fkpKSnJdYFh3bp1JabYFJUFCxYoLi5O/fr1U/369RUWFqa///3veRYyuRtKHkqE9u3ba+HCherbt6+cTqfWrFmj9u3bKzs7W06n06Pup/j888/f8MruvHnzijENSgqr1aqLFy+6XjtHjhxx63+citrVDW2veu2111x/T09PL+44bmfSpEkaO3askpKSFBISotKlSys2NtboWIZq2LChJk6cqHHjxmn79u1auXKlZs6cWeCiJndAyUOJMH/+fEnXF5i33nrL4+6n+MgjjxgdASVQRESEhgwZopSUFEVGRmrHjh2KiYkxOpZh7Ha7MjMzVb58eUlSvXr1JEmZmZmy2WxGRnMLAQEBWrlypY4dOyan06mAgACPH6696ujRo/r222+1f/9+3XfffUbHuSG2UAFgSqwivd7Jkye1Y8cOOZ1OBQcHq3bt2kZHMsybb76pw4cPa9asWa6il5mZqSlTpiggIECjR482OKExjhw5csPznrzf5AcffKC1a9fq4sWL6t27t3r16qVTp04pKCjI6GgFouTB7eXm5qpv376uW1bhitTUVH344YfX3XDe04drWUWKwrh8+bIiIyO1detW1alTR9KVBV3t27fXP//5T/n4eOZAV0hIiCwWi5xOp5KTk1W+fHlZLBalp6erRo0aHj13fMqUKQoLC1PNmjUVFxenuLg4OZ1Obd682ehoBfLMVzFKFG9vb5UtW1Y5OTkePYfo90aNGqV69eqpdevWDKNcg1Wk+du9e7def/11nThxQrm5uR5/hxQfHx/NmTNHx48f18GDByVJ9957r0df3ZT+twBw5syZCgoKUpcuXSRJGzdu1O7du42MZqjLly8rODhYCxcu1L59+3T58mUtWbJEgYGBRke7IUoeSoSAgAA9/vjj6tSpU55d6T15FVx6ejpXp/LBKtL8TZ48WS+88IIaN24sLy8vo+O4jdq1a3t8scvPd999p6lTp7o+7ty5sxYuXGhgIuPMmjVLn3zyie6++2717t1bb775pkJDQ92+4EmUPJQQubm5atCggY4ePWp0FLfRoEEDnT17VtWqVTM6ilthFWn+Klas6LoqA/wRp9Op3bt3u+ab/ec//5HD4TA4lTFWrFihwMBADR8+XK1atZJUcvauZU4eUEINGTJEBw4cUJMmTfKUGE+fk5eQkKCFCxfq5MmTatOmjWsV6YMPPmh0NEO9//77slqt6tKlS57XiydtP4TC2717t8aMGeN6feTk5Oi1115Ts2bNDE5W/NLT07V+/XqtXr1av/32m3r16qXVq1friy++MDraH6LkoURwOp1asWKFvv76a0lScHCw+vXrV2LeTRWFghai9O7du5iTuB9WkV4vPj5eU6dOVXZ2tiS55uR50vZDuDk2m01JSUmSrkyZsVqtBicy3k8//aTVq1crPj5edevWVffu3RUeHm50rAJR8lAiREdH68cff3Tdhmjt2rW65557NGHCBIOTASVDSEiI5s2bp/vuu485eSiUrKws/fLLL3k2jvbkLVSuZbfbtWXLFq1Zs0bvvPOO0XEKRMlDidC9e3fFxcW5tjWw2+0KCwvT+vXrDU5mjN27d+utt97Szz//LEm6++67NXLkSLfer6m4fP/994qJidHJkydZRXqN8PBwLV++3OgYKCGWLVumOXPmyM/P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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "##9) which is the busiest month for hotel booking"
      ],
      "metadata": {
        "id": "G_NCkpjxeFZp"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "\n",
        "df_not_canceled = df_Hotels[df_Hotels['is_canceled'] == 0]\n",
        "plt.figure(figsize=(18,6))\n",
        "new_order = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September',\n",
        "             'October', 'November', 'December']\n",
        "\n",
        "sorted_months = df_not_canceled['arrival_date_month'].value_counts().reindex(new_order)\n",
        "\n",
        "x = sorted_months.index\n",
        "y = sorted_months/sorted_months.sum()*100\n",
        "\n",
        "\n",
        "sns.lineplot(x, y)\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 432
        },
        "id": "-cqP8Ok6V77X",
        "outputId": "3e961b4c-5f83-4ee9-a68c-275f5c1374e3"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/usr/local/lib/python3.8/dist-packages/seaborn/_decorators.py:36: FutureWarning: Pass the following variables as keyword args: x, y. From version 0.12, the only valid positional argument will be `data`, and passing other arguments without an explicit keyword will result in an error or misinterpretation.\n",
            "  warnings.warn(\n"
          ]
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 1296x432 with 1 Axes>"
            ],
            "image/png": "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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "above line plot gives a conclusion that most of the busiest months are July and August"
      ],
      "metadata": {
        "id": "d40HOSoGOStM"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##10)Which is the busiest month for Resort and City Hotel?"
      ],
      "metadata": {
        "id": "Bg_tIAi5ezvI"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Select only City Hotel\n",
        "sorted_months = df_not_canceled.loc[df_Hotels.hotel=='City Hotel' ,'arrival_date_month'].value_counts().reindex(new_order)\n",
        "\n",
        "x1 = sorted_months.index\n",
        "y1 = sorted_months/sorted_months.sum()*100\n",
        "\n",
        "\n",
        "\n",
        "## Select only Resort Hotel\n",
        "sorted_months = df_not_canceled.loc[df_Hotels.hotel=='Resort Hotel' ,'arrival_date_month'].value_counts().reindex(new_order)\n",
        "\n",
        "x2 = sorted_months.index\n",
        "y2 = sorted_months/sorted_months.sum()*100\n",
        "# Draw the line plot\n",
        "\n",
        "fig, ax = plt.subplots(figsize=(18,6))\n",
        "\n",
        "ax.set_xlabel('Months')\n",
        "ax.set_ylabel('Booking (%)')\n",
        "ax.set_title('Booking Trend (Monthly)')\n",
        "\n",
        "\n",
        "sns.lineplot(x1, y1.values, label='City Hotel', sort=False)\n",
        "sns.lineplot(x1, y2.values, label='Resort Hotel', sort=False)\n",
        "\n",
        "plt.show()\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 499
        },
        "id": "lMnFz4WlXnUW",
        "outputId": "30c0fa35-3795-478c-aefd-a4a8914293da"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/usr/local/lib/python3.8/dist-packages/seaborn/_decorators.py:36: FutureWarning: Pass the following variables as keyword args: x, y. From version 0.12, the only valid positional argument will be `data`, and passing other arguments without an explicit keyword will result in an error or misinterpretation.\n",
            "  warnings.warn(\n",
            "/usr/local/lib/python3.8/dist-packages/seaborn/_decorators.py:36: FutureWarning: Pass the following variables as keyword args: x, y. From version 0.12, the only valid positional argument will be `data`, and passing other arguments without an explicit keyword will result in an error or misinterpretation.\n",
            "  warnings.warn(\n"
          ]
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 1296x432 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAABCMAAAGJCAYAAACw8PnnAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nOzdd3zV5fn/8deZ2YNMICSBEMLeYQnKENlDwFURUXFVbeuvttZv66iobe34ar/uFhBX6wYkhCFDUUSW7BUIkISVhEDIzlmf3x/BKLICnOQk4f18PHxIzvl87vs6FwHOuXLd920yDMNARERERERERKSOmH0dgIiIiIiIiIhcWVSMEBEREREREZE6pWKEiIiIiIiIiNQpFSNEREREREREpE6pGCEiIiIiIiIidUrFCBERERERERGpUypGiIiINAIHDx6kbdu2uFyuM547fPgw3bt3x+12+yCy2tG2bVuysrLO+fz777/Pc889V4cRnWnNmjVcc80153z+scce44UXXrjgOMeOHWPkyJE4HA5vhiciIuJTKkaIiIjUoSFDhtClSxe6d+9Or169uPfeezly5Eitztm8eXM2btyIxWLx6rh333033bt3p3v37nTs2JFOnTpVf/3kk096da6L4XA4eO2117j77ruBHwo1119//WnXHT9+nE6dOjFkyBCvzHuhAsmlioqKok+fPnzwwQdeH1tERMRXVIwQERGpY6+//jobN27k66+/JjIykmeeecbXIV2SGTNmsHHjRjZu3MjYsWOZNm1a9dfTp0+vvu5s3Rq1admyZSQlJREbG3va4+Xl5WRkZFR/nZaWRlxcXJ3GdqnGjh2rYoSIiDQqKkaIiIj4iJ+fHyNGjCAzM7P6seLiYh599FH69u3L4MGDefXVV/F4PAB4PB5effVVBg8eTL9+/Xj00UcpLi4+69iLFy9myJAhZGRknLGEY8qUKbz44ovccsstdO/enbvuuovjx49X3zt37lwGDx5Mnz59eOWVVxgyZAjffPPNRb22tm3b8t577zFs2DCGDRsGwIoVKxg/fjypqanccsst7Nq1q/r6IUOGMHPmTMaOHUvPnj15+OGHqaysrH5+xowZDBgwgAEDBvDxxx+fd+6VK1fSq1evMx4fP348c+bMOe11/rRbIjMzkylTppCamsro0aNZtmxZ9XOPPfYYTz/9NPfeey/du3fnxhtvJDs7G4DJkydXz9G9e3fS09Or75s1axb9+vVjwIABfPLJJ2eNecyYMSxfvrz6a6fTSZ8+fdixYwcAXbt2JScnh0OHDp33tYuIiDQUKkaIiIj4SHl5Oenp6XTt2rX6sWeeeYbi4mKWLl3KO++8w7x586o/wH766afMmTOHt99+m6VLl1JWVnZaB8L3PvnkE/7+97/z5ptvkpKScta509LS+POf/8zq1atxOp3MmjULgL179/L000/zt7/9ja+++oqSkhJyc3Mv6fUtXbqUDz/8kPT0dHbs2MHvf/97pk+fzpo1a7j55pt54IEHTtsHYeHChcyYMYNly5axe/duPv30U6CquDBr1ixmzZrFkiVLWL169XnnzcjIoFWrVmc8Pm7cONLT03G73ezdu5eysrLTcu90Orn//vvp378/33zzDY8//ji/+c1v2LdvX/U16enpPPTQQ6xbt46EhITqPR/ee+89AObNm8fGjRsZNWoUULXfQ3FxMStXruS5555j+vTpnDx58ozYxo8fz2effVb99ZdffklMTAwdOnQAwGq1kpCQcFoBR0REpCFTMUJERKSOPfjgg6SmppKamsqqVauYNm0aAG63m/T0dB555BGCg4Np0aIFd955Z/WH1Pnz53PHHXcQHx9PUFAQv/71r0lPTz9tGcRbb73FzJkzeeedd0hMTDxnDBMnTqRVq1b4+/szYsQIdu7cCcCiRYsYPHgwqamp2O12fvnLX2IymS7pdd57772Eh4fj7+/PBx98wM0330zXrl2xWCxMmDABm83Gpk2bqq+fMmUKsbGxhIeHM3jw4OqYFi5cyMSJE0lJSSEwMJCHHnrovPMWFxcTFBR0xuNNmzalVatWfPPNN8ydO5fx48ef9vzmzZspKyvj3nvvxW63069fPwYPHsyCBQuqrxk6dChdunTBarUybty46hjPxWq18uCDD2Kz2Rg4cCCBgYHs37//jOvGjRvHl19+SUlJCQCfffYZ48aNO+2aoKCgc3bCiIiINDQqRoiIiNSxV155hfXr17NlyxaefPJJpkyZQn5+PidOnMDpdNK8efPqa5s3b17dmZCXl3faHgdxcXG4XC4KCgqqH5s5cyaTJ0+madOm540hOjq6+tcBAQGUlZVVz/HjewMCAggPD7+k19msWbPqXx8+fJg333yzugiTmprK0aNHycvLq1FMPx7rQvs8hIaGUlpaetbnrr/+eubMmcOCBQvOKEZ8/9rN5h/eHv04/1C1meT3/P39q2M8l/DwcKxW61lf14/FxsbSo0cPFi9eTFFREStXrjyjGFFaWkpISMh55xMREWkoVIwQERHxEYvFwrBhwzCbzWzYsIEmTZpgs9k4fPhw9TVHjhyp3ogxJibmtD0DDh8+jNVqJTIysvqxWbNm8dprr7F48eJLiikmJua0D98VFRUUFhZe0lg/7qho1qwZ999/P+vXr6/+b/PmzYwZM6ZGMf34xJEf5+ds2rZty4EDB8763LBhw/jiiy9o0aLFaUWf7+c5evRo9R4dcHr+a9uECRP47LPPWLRoEd26dTttXpfLRXZ2Nu3atauTWERERGqbihEiIiI+YhgGS5cupaioiNatW2OxWBgxYgQvvPACJSUlHDp0iDfffLP6J+RjxozhrbfeIicnh9LSUl544QVGjhx52k/ek5OTmTFjBtOnTz9t88WaGj58OMuXL+e7777D4XDw0ksvYRjGZb/WG2+8kffff5/NmzdjGAZlZWV88cUX1csSzmfEiBHMmTOHvXv3Ul5ezssvv3ze6wcOHMi6devO+lxgYCBvvfUWzz333BnPdenSBX9/f2bMmIHT6WTNmjUsX768ev+HC4mKiiInJ6dG157N0KFD2bFjB2+//fYZG2tu2bKFuLi4BnP6h4iIyIVYL3yJiIiIeNP999+PxWIBqpYc/OUvf6FNmzYAPPHEEzzzzDMMHToUPz8/brzxRiZNmgTApEmTyM3N5bbbbqOyspIBAwbwxBNPnDF+u3bteP3117nvvvuwWq20bt26xrG1adOGJ554gl//+teUl5dz++23ExERgd1uv6zX3LlzZ5555hmmT59OVlYW/v7+9OjRg9TU1AveO3DgQKZOncrUqVMxmUw8/PDDzJ8//5zXDx48mD/96U/k5uaetauhc+fOZ73Pbrfz+uuv8/TTT/PGG28QGxvLX//61xrn76GHHuKxxx6joqKC6dOnn9axUhP+/v4MGzaMBQsWcN1115323Pz587nlllsuajwREZH6zGR448cdIiIi0iiVlpbSq1cvFi9eTHx8vK/DqbEPPviAvXv38oc//MHXoVyUl19+mQMHDvD3v/+9+rGCggJuu+025s6di5+fnw+jExER8R4VI0REROQ0y5cvp1+/fhiGwV/+8he2bNnCnDlzLvlUDamZwsJCJkyYwF//+ld69erl63BERERqlfaMEBERkdMsW7aMq6++mquvvpqsrCz+93//V4WIWvbhhx8yaNAgrr76ahUiRETkiqDOCBERERERERGpU+qMEBEREREREZE6pWKEiIiIiIiIiNQpFSNEREREREREpE5ZfR2AN5w4UYrH03C2voiMDKagoMTXYTQKyqX3KJfeo1x6j3LpPcql9yiX3qNceo9y6T3Kpfcol97TEHNpNpto0iTonM83imKEx2M0qGIE0ODirc+US+9RLr1HufQe5dJ7lEvvUS69R7n0HuXSe5RL71Euvaex5VLLNERERERERESkTqkYISIiIiIiIiJ1SsUIEREREREREalTjWLPCBEREREREWlc3G4XJ07k43I5fB2Kz+XlmfF4PL4O46zMZgsBAcEEB4dhMplqfJ+KESIiIiIiIlLvnDiRj79/IEFBTS/qQ25jZLWacbnqXzHCMAzcbhfFxYWcOJFPRERMje/VMg0RERERERGpd1wuB0FBoVd8IaI+M5lMWK02wsMjcTgqLupeFSNERERERESkXlIhomEwmczAxR09qmKEiIiIiIiIyAW4XC5mzHidW26ZyNSpt3Dnnbfy0ksv4HK5+PrrL3nllX8CcOTIYebN+/SS5njooXtZteqr0x57/PFHSUv77IL3pqfPJzs7q0bzzJz5Bi+//OIlxegt2jNCRERERERE5AL+9KenqaysYNasdwgMDMLlcrFgwWc4HA4GDBjIgAEDgapixGefzWH8+Il1Gl96+nzCwsJJSEis03kvlTojRERERERERM4jJyeblStX8LvfPUFgYBAAVquV8eMnEhgYSHr6fB5//FEA/vd//8qBA/u4445befzxR1m+fCm//e2vqsdyOByMHz+co0ePXnQcZWVl/OlPTzNlyk1MmXIT7733FgALFnzG7t07efHFv3PHHbeybt0aAN59dzb33HM7d901mUcf/X8UFBy73FR4jTojREREREREpF5btfUIX285UitjD+jSjP6dm533moyM3bRokUBoaOgFx/v1rx/llVf+ycyZ7wBVyzteeeVFDh8+RPPmcSxf/jkdOnSmadOmZ73/xRf/zr///Vr110ePHmbAgGsAmD17Bh6Ph7ff/oCyslLuu+8ukpKSGT16HAsXpvGzn02hf/+rAVi8OJ1Dhw7xxhuzMZvNzJnzMS+//CJPPfVsjfJS21SMEBEREZE6t2F3HhvSdnDjwNY0CfHzdTgiIrXm+w6KuXM/4YEHfsmnn37EPff8/JzXP/zwb6oLCkB1xwXA+vVr+dWvfoPJZCIoKJihQ4exfv1a+vXrf8Y4X3+9kl27dnLXXbcB4Ha7CA4O9uIruzwqRoiIiIhInSmtcPLe5xl8uz0XgPzjZTx6aw9sVq0eFpFz69/5wt0LtSklpS0HD2ZTVFRUo+6Inxo3biJ33TWZAQOuoaSkmNTU3rUQ5ekMw2Dq1LsYM2Z8rc91KfS3voiIiIjUiW37C3hy5lrW7cxj/IBW/Pa2nmQeLuKdJbsxjIs7Ek5EpC7FxyfQv/81/O1vf6KsrBQAt9vN/PlzKSsrO+3aoKBgSktLTnssPDyc1NTe/PGPf2DChBsv+cjS1NTeLFgwD8MwKCsrZdmyJfTq1efUvEGnzTtgwDXMmfMxRUVFQNVeFXv2ZFzSvLVBnREiIiIiUqsqHC4+WpHJio2HaB4VxC8mdaZl01Cio0PYue8Yad9k0bJpCEN6tPB1qCIi5/T4408za9a/uOuuKdhsVgzDoG/f/tjt9tOua906mYSERKZMuYnExJY8++xfARgzZjwrVixl5MgxlxzDHXfczQsv/JXbb78ZgOHDR9G371VAVffFyy+/wH/+8w4PPvgrRowYzcmThfziF/cC4PF4mDDhRtq0Sbnk+b3JZDSCMnRBQQkeT8N5GdHRIeTnF/s6jEZBufQe5dJ7lEvvUS69R7n0HuXy4uw5WMjMtJ3kF5YzrHc8E69Jwma1AFW5zM0r4qWPt7Bt/3F+c0s32iY08XHEDZO+L71HufSey83l0aNZNG3aMI6prInZs2dQUFDAI4/87qLvtVrNuFyeWojKe376+2U2m4iMPPceFVqmISIiIiJe53R5+GjFXv7y7nd4DINHb+3OzUPaVBcivmc2mbhnbEeiwwN4de42jhdV+ChiEZHac9ttN7FixTLuuGOar0OpN7RMQ0RERES8Kju3mH+n7eBQfikDuzXnpsHJBPid+21noL+VX0zqzDNvreelT7fyP5N7YLdZznm9iEhD8+67H/o6hHpHnREiIiIi4hVuj4f5q/bzzFvrKSl38vCNXZg6ot15CxHfaxYZxL1jO5J1tJi3Fu3ShpYiIo2cOiNERERE5LIdKShlRtpO9h8ponf7GG4b1pbgANtFjdGtTRTXX92KuV/tJzE2hGG9E2opWhER8TUVI0RERETkknkMg2UbDvLxF5nYrWbuH9+R3u1jL3m8MVe1JDu3hA9W7CUuJpiOLSO8GK2IiNQXWqYhIiIiIpfk2Mly/v7fjfx36R7aJzbhmbv7XFYhAqo2tJw2uj3NI4N4fe428gvLvRStiIjUJypGiIiIiMhFMQyDr7Yc5smZa9l/tJg7RrbjVzd0ITzYzyvjB/hZeWhSZwwDXvpkK5UOt1fGFRGR+kPFCBERERGpsZMllbz0yVbeTN9FYmwIz9zVm2u6NsdkMnl1ntgmgdw/viOHjpUwK32nNrQUEZ+74Yax3HrrJKZO/RmTJ9/A/Plz62zu999/jxMnjp83tn379p722LRpU/juu/UXHPvDD/9z3rF/7Lnn/sgnn3xQo2svRHtGiIiIiEiNrN+Vx9uLd1PpdHPLtW0YmtoCs5eLED/WKSmSGwa25qMvMklsGsKovom1NpeISE08++zzJCUls2/fXu666zb69etPVFR0rc3n8XgwmUy8//5/6NGjF02aeH8fnQ8//C+pqb1rZezzUTFCRERERM6rtMLJe0sy+HZHLi2bhnD3mA40jwqqk7lH9EkgK7eYT77IJD4mmM5JkXUyr4jI+SQlJRMSEkp+fh5RUdFkZx/gn//8X06eLMTpdHLTTT9j9OhxVFRU8OyzT3HgwD4sFisJCYk888xfAHj33dksXpwOQPv2HXn44d8SGBjIzJlvsH//PkpLS8jNPcrw4aM4diyfxx//HXa7H0899SytWiVdVLzHjxfwt7/9mcOHD2IYBj/72RRGjhzDW2/NPGPsFi3i+de/XmXTpg04HE6Sk5N55JH/ITAw0Ks5VDFCRERERM5p274CZqXvpLjMyfVXt2JU30Sslrpb6WsymbhzZHuOFJTx+rztPDk1ldgI774hFpH6z5mxCufulbUytq3tNdhS+l/UPVu2bCIsLJzk5BRcLhd//OPjPPXUsyQmtqSsrJRp06bQqVMXDhzYT1lZKe+++xEARUVFAKxevYrFi9N5/fVZBAYG8eyzTzF79gweeOCXAOzYsY1Zs94jPDwcgPnz51Z3ZZzL9wWF7+XkZFX/+sUX/05SUmv+/Oe/c+zYMaZNu422bdsxdeq0M8aePXsGQUFB/PvfbwPw6qv/xzvvvMl99z14UTm6EBUjREREROQMFQ4XH67I5IuNh2geFcSvbuhKYtMQn8TiZ7fwi4mdmf7Wev7vky08fnsqAX56Gyside/xx3+HYRgcOnSQZ575Czabjf3795GVtZ+nnvp99XVOp5MDB/aTnNyGAwf2849/PE/37j256qoBAKxfv5Zrrx1GUFAwAOPGTeSf//x79f39+vWvLkTU1E+LFdOmTan+9fr1a3nooYcBiIqKol+//nz33fqzFjdWrVpJaWkpX3yx/NRrcZCc3OaiYqkJ/S0uIiIiIqfJyClk5oIdHCusYETvBCZc0wqb1XLZ4xpuJ55jWbjzMnHnZnLYVYpl4H2YA0IveG9UeAA/H9+Rf3ywmRlpO3hwYuda3a9CROoXW0r/i+5eqA3ff+Bfvnwpf/rT03Tu3BXDMAgLC2f27P+c9Z533/2Q9evX8e23q/jXv17hrbfev+A8AQG+6wAzDHjkkcfo2bNXrc6j0zREREREBACny82HK/by/HvfYRjwu8k9uGlI8iUVIgzDwFOcj3Pvt1R88x6lc6dT8ubPKZv3LJWr/4s7dy8V2Ttwbl1S4zHbt4zg5iHJbNxzjLRVBy46JhERbxkyZCi9evXlnXdmk5CQiL+/P4sWLah+PivrAKWlJeTl5WI2W7jmmkH88pePUFh4guLiIlJTe7N8+eeUlZViGAZpaXPp1avPOecLCgqipKTkkuNNTe1dffpHQcExVq9eRY8evc469oAB1/DBB+9RWVkBQFlZKQcO7L/kuc9FnREiIiIiQtbRYmak7eDQsVIGdWvOTUOS8bfX/K2i4azAnb8fd14mntxM3HmZGOVVa6Ox2LHEtMLeeRjmmNZYYpIwBzXBs/INSncsw95tFCZ7zX4KODS1BVm5xcz9ej/xscF0b1N7u9iLiJzP/fc/xLRptzF58lSef/4F/u///sF///sObreHiIgIpk//C5mZe3n99ZcB8Hjc3HbbHURFRRMVFU1m5h7uu+9OANq168DUqdPOOddNN/2MP/1pOv7+/pe0geXDD/+Gv/3tT0ydeguGYXD//Q+RlNQagBtuuOW0sW+77Q5mznyDu+++HbPZDJi46657aNmy1aUl6hxMRiM4tLmgoASPp+G8jOjoEPLzi30dRqOgXHqPcuk9yqX3KJfeo1x6T2PLpdvjYcHqLOavOkBIoI07R7W/4IkVhuHBOJlbvdzCnZeJ53hOVW8vYAqLxRLTuuq/2GTMEXGYzGcWNkJd+Rya9VvsvW/Ar9uYGsfscLr5y3vfcfR4GY/fnlpnJ3vUZ43t+9KXlEvvudxcHj2aRdOmOtIXwGo143J5fB3Gef3098tsNhEZGXzO69UZISIiInKFOlJQyoy0Hew/UkyfDrFMvi6F4ADbGdcZlaW48/ZVFR/yMnHn7YPK0qonbQFYYpKwdx9bXYAw+Z/7zeeP+TVLwtKiE86tS7B3GobJaq/RfXabhYcmdmb67HW89MkWnpiaSqD/mXGLiEj9pWKEiIiIyBXGYxgsXX+QT77MxM9m4efXd6JXuxgADI8Hz4mDP3Q85GXiKTxy6k4T5og4bK1SscS0xhzbGnN4M0ymS9+GzN59LOXz/4xz90rsHYfW+L6IUH8emNCZv/13I/+av4NfTuqC2awNLUVEGgoVI0RERESuIMcKy5mVvpNd2YV0bR3JHYOaE1R6kMq1K3/oenBVAmDyD8Ec0xp7m6uquh6iW2GyB3g1HkvTFMyxyTg2L8TWftBZl3OcS0p8OLcObcM7SzKY89U+Jg1s7dXYRESk9qgYISIiInIFMAyDrzfl8NWXa0mw5HNLm3IiHEcw5uRTDmCyYI5KwNZ2QPVeD6aQaEy1fHymyWTCr/sYyhe9iGvvmos+um9Q9ziycktYsDqLhNiQ6g4PEWkcDMOo9b+H5PIZhge4uN+nOilGPP/88yxevJhDhw4xf/58UlJSzvu4iIiIiFwewzAwSo/jzs2k/OBu8vbuoKMrl26BVRugmSoisMQkYek4BHNMMpaoxBrv2eBtlviumCPicWxagLVNv4ta9mEymZh8XQqHjpUwc8EOmkYEEh9Tsz0rRKR+s1rtlJYWERQUqoJEPWUYBm63i+LiE9jt/hd1b50UI6699lpuv/12Jk+eXKPHRUREROTiGK5K3PkH8PzohAujrBAAl2GhzB2Ju3k/WnXphjWmNebgCB9H/AOTyYS922gqlr+OK2sjtpY9L+p+m9XMgxM68/SpDS2fvKPXWTfiFJGGpUmTaE6cyKekpNDXofic2WzG46mfp2mYzRYCAoIJDg67qPvqpBiRmpp6UY+LiIiIyLkZhoFRlFtddHDnZeIpyAHjVNdDaAxGbFvWHwvmi4N+2KMTuGtsZ5pF1t8jMK1JvTCt/xTHxjSsiT0u+qeg4cF+PDShM8//5zvemLeNh2/qisV86RtriojvWSxWoqKa+TqMeqExHjmrPSNERERE6jnDUYY7bz/uvL24czPx5O3DqCypetLmX3W0ZrfRVSdcxCSx7bCTNxfupKTMybj+LRnVL7HefzA3mS3Yu46i8qvZuA/vxBrX4aLHaB0XxpRhbXlz4S4+/iKTm4e0qYVIRUTEGxpFMSIysuGtC4yODvF1CI2Gcuk9yqX3KJfeo1x6j3LpPbWZS8PjxnnsEBWHMqg8lEHF4Qyc+QcBAzBhi25BYLs++MWl4B+Xgi0qDpPZAkB5pYuZn21j8bdZJDYN4el7+tG6RXitxeoNP86l0WQE2RvnYWxfSHS3Ppc03sShbckrqmTBqv10So5mUM94b4Va7+nPuPcol96jXHpPY8tloyhGFBSU4PEYvg6jxhpji42vKJfeo1x6j3LpPcql9yiX3uPtXHrKi/Dk7atebuHO2wfOiqon/YKwxLTGnppadcJFTBImeyAAlaf+o6AMgIycQmak7aDgZAUj+yRw/dVJ2Kzmev37frZcWjsNo+LbDzi6fROWmEs7qnP8VYnsyT7B/324iWC7hcSmjesN/Nnoz7j3KJfeo1x6T0PMpdlsOm/jQKMoRoiIiIg0BIbHhafgYPVyC3deJkZRXtWTJjPmyHhsba46dbRma0yhsRfcO8HpcvPpyn0sWZtDVLg/v5vcg5T4+t0NcT629oOp3JiGY2MaAcN/dUljWC1mHri+E9PfWsdLn27hyam9CA3yzUkhIiJydnVSjHj22WdZsmQJx44d48477yQ8PJwFCxac83ERERGRxsBTegJ37t6qDSbz9uHO3w9uJwCmwPCqokP7QZhjWmOJbonJ6ndR4x84WsSMtJ0cPlbKoO5x3DS4Nf72hv2zJpPNH3vHoTi+m4f7+CEsEXGXNE5okJ2HJnbmz+9+x2tzt/HILd2wWur3vhkiIlcSk2EYDWd9wzlomcaVS7n0HuXSe5RL71EuvUe59J5z5dJwOXAfy8JT3fWwD6P0eNWTZivm6Janllqc6noIirjoEyO+53J7SF+dxfxvDhASaOOuUe3plBR5OS/LJ86Zy4oSSv7zCNZWPQkYfO9lzbF621H+nbaDa3u2YPJ1KZc1Vn2mP+Peo1x6j3LpPQ0xl1qmISIiIuJlhmFgFOdX7fGQ+/3RmtngcQNgConG0jQFS2xV8cEcGY/JYvPK3IePlTIjbQcHjhbTt2Msk69LIcjfO2PXFyb/YGztB+Hc9jmenhMwh0Zf8lj9OjUlK7eYJetySIgN5uouzb0YqYiIXCoVI0RERERqyFNynKNfvkZ51g6MilM/obL6VR2t2WVk9dGa5sAw789tGCxdl8PHX+7D327hges7kdouxuvz1Bf2LiNwbl+KY8tC/Afcfllj3Ti4NTl5JbyzeDfNo4Jo3dz7vz8iInJxVIwQERERqaHKtR/hPrARS1LvU8stkjE3aV59tGZtOVZYzswFO9mdU4wmZE8AACAASURBVEi35CimjmxHWCPfkNEc1ARbygCcu1di7zEOc+Clb8ppMZv5+fWdmD57Ha98upUn7+hFePDF7c8hIiLepV18RERERGrAU3gUV+a3hKaOJGDQ3dg7DMYSGV+rhQjDMFi5+TBPzFpLVm4xd41qzy8mdW70hYjv2buOAo8b59Yllz1WcICNX0zqQlmli1fmbMXp8nghQhERuVQqRoiIiIjUQOXGz8BiI7zv+DqZr7Ckkn9+vIXZC3fRqmkI06f1ZkCXZpe86WVDZA6LxZrUG8eO5RiVpZc9XnxMMNNGdyDzUBH/WZrhhQhFRORSaZmGiIiIyAV4Co/i2rsaW+fhWILCoKx2dzRfuzOXdxbvxuHycOvQNgzp2QLzFVSE+DF7t9G4Mtfg2L4Mvx7jLnu8Xu1iyO6XyILVWSTGhjCo+6UdHSoiIpdHxQgRERGRC6jcOB/MNuxdRtbqPCXlTt5dspu1O/No1SyUu8e0p1lkUK3OWd9ZIhOwJHTFue1z7F2GY7Je/l4PE65OIju3hPc+z6B5VBAp8Ze+H4WIiFwaLdMQEREROQ/PyaO49n6DreOQWjkl43tbMo/xxIw1bNidz4Rrkvj9lB5XfCHie/ZuYzAqinHuWumV8cxmE/eN60BUmD+vzt3G8aIKr4wrIiI1p2KEiIiIyHnUdldEeaWL2Qt38eJHWwgOtPHE1FTGXtUSi1lv075nbdoGS7O2ODYvxHC7vDJmoL+NhyZ1odLpPrWhpdsr44qISM3oXzkRERGRc/CczMW1ZzW2DoNrpStid/YJnpq1lq+2HGZk3wSenNqLhNgQr8/TGNi7jcYoPY5r72qvjRkXFcS9Yzqw/0gxby/ajWEYXhtbRETOT8UIERERkXOo6oqwYO/q3a4Ip8vN+8v28Nf/bMRsMvHY5B7cOCgZm1Vvzc7F0qIz5shEHJsWYHi8dyxn95Roxg9oxaptR1m64aDXxhURkfPTBpYiIiIiZ1HVFfENtk7XYQ703gaH+48UMSNtB0cKyhjcI44bB7XG3663ZBdiMpmwdx9NxdJXcR3YgC2pl9fGHtu/Jdm5xXywbC8tooNpn9jEa2OLiMjZqfwuIiIichbe7opwuT3M/Wofz729gQqHm1/f3JUpw9qqEHERrC1TMYU1xbEpzatLKswmE3eP6UBsRACvzd3GscJyr40tIiJnp2KEiIiIyE94ivKquiLaD/ZKV8ShY6U8984GPlt1gD4dYpg+rTedWkV6IdIri8lsxq/rKDzHsnAf3ObVsQP8rPxiUhfcHoOXP91KpVMbWoqI1CYVI0RERER+ovK7U10R3UZd1jgej8GiNdk8/eY6Ck5W8OCETtwztiNB/jYvRXrlsba5ClNQBI5NaV4fu2lEIPeN60BOXglvpu/UhpYiIrVIxQgRERGRH6nqiliFrf2gy+qKyC8s56//3ciHK/bSOSmCZ+7uQ8+2MV6M9MpkslixdxmB+8hu3Ef3eH38Lq2jmDgwibU781i0Ntvr44uISBUVI0RERER+xPH9XhHdRl/S/YZh8OWmQzw5ay05ecVMG92ehyZ2JizI7uVIr1y2dgMx+QVTWQvdEQCj+iaS2i6Gj7/IZNu+glqZQ0TkSqdihIiIiMgpnqI8nBnfXHJXxIniSl78aAtvLdpNUrNQpt/Vh/6dm2EymWoh2iuXyeaHrfMw3NmbcRfkeH98k4lpo9oTFxXE6/O2k3uizOtziIhc6VSMEBERETnFsTENzCbsXS9+r4g1O3J5cuYadmefYPJ1KTxySzciw/xrIUoBsHe8Fmz+ODYtqJXx/ewWHprUBZMJXv5kKxUOV63MIyJypVIxQkRERATwFOXjzFiFrd0gzEFNanxfSbmT1+Zu443PttM0IpA/3tWba3u2wKxuiFpl8gvC1n4wrn1r8BTl1cocMeEB3H99Jw4XlDIzTRtaioh4k4oRIiIiIoBj0/yqroiL2Cti895jPDFjDd9l5DNpYBKP3daDphGBtRil/Ji9y3AwW3BsSq+1OTq2jOCmwclsyMgnbXVWrc0jInKlsfo6ABERERFf8xTn49y9CluHmnVFlFe6eH/ZHr7acoQW0UH8v5u6khAbUgeRyo+ZA8OxpVyNc/dX2HuOv6iOlosxrFc8WbnFzF25j/iYYLolR9XKPCIiVxJ1RoiIiMgVz7ExDUwm7N3GXPDarZnHeGrWWr7eeoRRfRN5YmovFSJ8yN51JBgeHFsX19ocJpOJO0a0IyE2hH/P386RgtJam0tE5EqhYoSIiIhc0TzFx3Du/hpbu4Hn/cl61tFiXp2zlT+8tgqz2cT/TO7JDYNaY7Pq7ZQvmUNjsLbug3PHCoyKklqbx26z8NDEzlgtZl76ZCtlFdrQUkTkcuhfTxEREbmi/dAVceZeEYZhsCvrBP/4YBNPz17H9gMnuPHaFJ6+szfJLcJ8EK2cjb3baHBV4ti+tFbniQzz54HrO5FfWM6/52/How0tRUQumfaMEBERkSuWp/gYzoyvqroigiN+eNww2LznGAu+zWLf4SJCg+zcOKg1g7rHkdCiCfn5xT6MWn7KEtECa2J3HNs+x95lBCZb7R2p2jahCbdc24b3Ps9g3lf7mXBNUq3NJSLSmKkYISIiIlcsx6Y04IeuCJfbw9qduSz8NptDx0qJCvNnyvC2DOjcFJvV4ttg5bzs3UbjmrcR584vq07ZqEVDesSRlVvM/G8OkBAbTM+2MbU6n4hIY6RihIiIiFyRPCUFOHdXdUW4/ML5asNBFq3JpqCoghbRQdw7tgO92sdgMWtVa0NgiU3G0rw9ji0LsXUcgsliq7W5TCYTU4alcPhYKTPSdhIbEUiL6OBam09EpDHSv64iIiJyRXJsTAPgK1dXfvvaN7z3eQZNQv341Q1dePqu3vTt2FSFiAbG3m00Rlkhzj3f1PpcNquFByd0xt9u4eVPtlJS7qz1OUVEGhP9CysiIiJXnJO5R6jc+SXfVibz328LaNk0lMcm9+D3t/Wka3IUJpPJ1yHKJbDEdcQc3QrHpnQMj6fW52sS4seDEzpTUFTBG59tx+PRhpYiIjWlYoSIiIhcMfIKy3l78W5WfzgbjwFHmg3kj3f24v/d1JWU+HBfhyeXyXTqVBSjKBfX/nV1MmdyizBuG5bC9v3H+eTLzDqZU0SkMdCeESIiItLoHcwrIf3bLNbuzCPCUsrvQ/fiSbqK24de5evQxMusLXtgDm+GY1Ma1qTeddLlMrBbHNm5JSxck01CbAh9OsTW+pwiIg2dihEiIiLSaO05WEj66iw2ZxbgZ7cwrFc8w01fYc6E0D7X+zo8qQUmkxl7t9FUfDEDd84WrAld62Tenw1tw8H8Et5M30mzyEASYkPqZF4RkYZKyzRERESkUTEMgy2ZBfzl3Q38+d3vyDxcxISrW/H3B67iht4RmDNXYUu5GnNIlK9DlVpiTe6LKTiyepPSOpnTYuaBCZ0JCrDx0idbKS5z1NncIiINkYoRIiIi0ih4PAZrd+by9JvrePGjzRwrquBnQ9vwt59fxdj+rQjyt+HYtAAMA3v3Mb4OV2qRyWzF3mUk7tw9uI7srrN5w4LsPDSxMydLHbw2dxvuOthEU0SkoaqTYsTzzz/PkCFDaNu2LRkZGdWP79+/n5tvvpnhw4dz8803c+DAgboIR0RERBoRp8vDF5sO8ft/fcvr87bjdHu4a1R7/nJfP65LjcfPbgHAU3oC564vsbUdoK6IK4Ct3dWY/EOqClB1qFWzUKaOaMuu7EI+WL63TucWEWlI6mTPiGuvvZbbb7+dyZMnn/b4U089xa233sr48eOZN28eTz75JG+//XZdhCQiIiINXHmliy83HWbxumxOljho1SyEBwd3pntKFOazbFro2JSmrogriMnqh63zcBzrPsZ9LAtLVGKdzd2/czOycotZuv4gibEh9O/crM7mFhFpKOqkGJGamnrGYwUFBezYsYM333wTgDFjxvDMM89w/PhxIiIi6iIsERERaYCKyxwsXX+Q5d8dpLTCRfvEJtwzpgPtE5uc8+SEH7oi+mMOia7jiMVX7B2H4Ni0AMemBQQMfaBO5755SDKH8kt5a9FumkcF0apZaJ3OLyJS3/nsNI0jR44QGxuLxVLVOmmxWIiJieHIkSMqRoiIiMgZjhdVsGhNNis3H8bp8tAjJZpR/RJr9CHPsWkBeAzs3cbWQaRSX5jsgdg7Xotj0wI8hUcxhzets7ktZjP3j+/I9NnrefnTrTx5Ry/Cgux1Nr+ISH3XKI72jIwM9nUIFy06Wsc9eYty6T3Kpfcol96jXHpPQ81lTm4xn6zYwxcbDgIwqGcLJg1uQ3wNj050FR8nZ9eXhHQZRHTrJK/E1FBzWR/Vdi7dgyaSvW0J5t2fEz2mbrsjooEn7+7Lb1/6in+n7eDZ+/tjs9belm36vvQe5dJ7lEvvaWy59FkxolmzZuTm5uJ2u7FYLLjdbvLy8mjW7OLX1BUUlODxGLUQZe2Ijg4hP7/Y12E0Csql9yiX3qNceo9y6T0NMZf7jxSRvjqL7zLysVnNDO4ex/DeCUSG+QPU+PVUfPMhhseDp/1wr+SgIeayvqqbXJqxtr2a4q1f4Ok4GnNw3XbghtjN3DmyHW98tp2X3v+OKcPb1so8+r70HuXSe5RL72mIuTSbTedtHPBZMSIyMpL27duTlpbG+PHjSUtLo3379lqiISIicgUzDIOdWSdYsDqLnVknCPSzMuaqllyb2oLQwItvcfeUFeLc+QW2lKswh8bUQsTSENi7jMS54wscWxbhf9WtdT5/nw6xZOcWs3BNNgmxwQzsFlfnMYiI1Dd1Uox49tlnWbJkCceOHePOO+8kPDycBQsW8Mc//pHHHnuMV199ldDQUJ5//vm6CEdEROo5wzD4eusRvttzjJiwAFLiw2kTH3ZJH0alYfAYBhszjpH+7QH2HykmLNjOTYOTGditOQF+l/52pWqvCDf27tor4kpmDonCmtwX564vsPcYi9m/7ludJw1sTXZeCe8uySAuKpjkFmF1HoOISH1iMgyj4axvOAct07hyKZfeo1x6j3J5efJOlPHWot3szDpBs8ggjp0sx+nyANAsMpCU+HBS4sNpGx9ORKi/j6NtOOrr96XL7WHNjlzSv83iSEEZMeEBjOibQP9OTbFZLZc1tqeskNL//hZr674EDJrmpYjrby4borrMpfvEYco++gP2HmPxS51YJ3P+VGmFk2dmr6fS6ebJO3rRJMTPa2Pr+9J7lEvvUS69pyHmst4u0xAREfkxt8fDkrU5zP16P1aLiduHt2XS0Lbk5hVx4GgxGTmFZOQUsnZnHl9uOgxAZKj/qeJEGCnx4TSNCDzn0Y5Sv1Q63azcfJjFa7M5XlRJfEww943rSGq7aCxm72zw59iUDh43fj3UFSFgadIca8seOLYtxd5lJCZ7QJ3HEORv4xeTOvPs2xt4+dOtPDa5+2UX3UREGioVI0RExOeyjhbz5sKdZOeW0CMlmsnXpdAkxA+z2YTVYiY5LozkuDBG9U3E4zE4mF9SXZzYvr+A1duPAhAaaKPNqc6JlBbhxMcEYzarOFGflFY4Wb7hIJ+vP0hJuZOUFmHcPrwdnZMivFpIqtorYgXWNtorQn5g7zYa14ENOHeuwN51lE9iiIsO5u4x7XllzjbeWZLBnSPbqYgqIlckFSNERMRnKp1u5n21n8XrsgkNsvPghE70bHv+D45ms4mE2BASYkMYmhqPYRjkniivLk5k5BSyYXc+AAF+FpLjqjon2sY3oWWzEKyW2jtWT86tsKSSJWtzWLHpEJUON11aRzK6XyJtWoTXynyOzQuruiK0V4T8iCUmCUtcRxxbFmPrOBST1Tf70PRsG8PYq1oy/5sDJMaGcG3PFj6JQ0TEl1SMEBERn9h+4DhvL9pFfmEFA7s158ZBrQn0t130OCaTiaYRgTSNCOSars0BOF5U8UNx4uBJPvmyAACb1Uzr5qG0aRFOSkI4yc3D8LOrRbo25Z0oY+GabFZtPYLbY9CnfSwj+yYSH3PuNaSXy1NWiHPHcqxt+mEOi621eaRhsncfQ3na8zgzvsbeYYjP4hh/dSuyc4t5f9keWkQH0Tahic9iERHxBRUjRESkTpWUO/lg2R5WbTtKbEQgv7u1u9ffhEeE+tO3Y1P6dmwKQFGZgz05J9lzsJDdOYWkrT6A8Q1YTnVZtD11WkebFuEEB1x8QUTOlJ1bTPq3WazblYfFbGZAl+aM6JNATHjtr9P/oStiXK3PJQ2PpVk7zDFJODYvxNZuICazbwqSZpOJe8Z25Nm31/Pq3G08ObUXkWHalFdErhwqRoiISJ0wDIM1O3P579I9lFW4GHNVImOvalknm7eFBtrp2Taanm2jASivdJF56CS7cwrZk1PI0g05LFqbDUBcdFD1nhMp8eFe3e3+SpCRU0j6t1lsySzA325hRO8ErusVT3hw3eTRU3YS544VWJPVFSFnZzKZ8Os2lvIl/8SVuQZbm6t8Fkugv/XUhpbreenTLfzPbT3xs6lbS0SuDCpGiIhIrSs4WcE7S3azJbOAVs1CueOWdrXapn8hAX5WOiVF0ikpEgCny83+I8XVxYlvth1lxXeHAIgJD6DNqdM6UuLDiQkP0GZzP2EYBlsyC1jwbRZ7D54kJNDGxGuSGNIj7pKW3lwOx5aF4HHqBA05L0tiV8xN4nBsSsea3BeTyXd7yTSLDOKesR156eMtvLVoF/eM6aC/Y0TkiqBihIiI1BqPx2DZdwf59Mt9APzs2jZc27NFvTvhwma1VBcboOqY0ezcEvbkVC3r2Ly3gFVbq07sCAu2Vy3raBFO2/hwmkcHYb5CPzi4PR7W7cojfXU2B/NLiAz1Y/J1KQzo0swnP931lJ3EuX051uSrMIc1rfP5peEwmczYu42mYsW/cGdtxtqyu0/j6ZYcxfXXJDFn5T4SY0MY3jvBp/GIiNQFFSNERKRWHMwvYfbCXew7XETnpEimDE8hKqz29wvwBovZTKtmobRqFsqw3gl4DIMjBWVknOqc2J1TyNqdeQAE+VurNsQ8te9EYmzjP7HD6XLz9dajLFqTRX5hBc2jgpg2uj19OsT69LWrK0IuhrV1H0zrP6VyUxqWxG4+70YY0y+R7NxiPlyxlxYxwXRsGeHTeEREapuKESIi4lVOl5v532Sx8NssAvys3Du2A306xPr8jf7lMJtMxEUFERcVxODucRiGQcHJiqplHQcL2Z1zkk17jwFgt5lp3Tzs1KaY4SQ1D200a8DLK118sfEQS9blcLLUQVLzUG4Z0oaubaJ83h3iKS861RXRT10RUiMmswV711FUfv027iO7sDZv79t4TCamjW7P0eNlvD53G0/c0atONnwVEfEVFSNERMRrMnIKmb1wF0ePl3FVp6bcPCSZkEC7r8PyOpPJRFR4AFHhAfTv3AyAkyWV7Dn4w6aY877ej0HViR0tm4WQEl+1rCM5LpxA/4b1z29RqYOlG3JYvuEQZZUuOrZswr3jOtIuIbzeFJmqTtBw6gQNuSi2lAE4NszFsTHN58UIAH+7lV9M7Mz02et5+ZMt/GFKqo4fFpFGq2G9GxIRkXqprMLFx1/s5YtNh4kK8+fXN3elU6tIX4dVp8KC/UhtF0NquxgAyiqc7Dl4koyDhWTkFLJkbQ4Lv83GBMTHBNPmVHGiTXw4YUH1s2Bz7GQ5i9fk8NWWwzhdHnq2jWZk30RaNQv1dWin8ZQX4dyxDGvrvpjD1RUhNWey2rF1HoFj7Ye48/djiW7l65CIaRLI/eM78sJHm5mZvpOfj+9Yb4p+IiLepGKEiIhclg2783n3890UlToY3jue6wck6Sd5QKC/ja7JUXRNjgKg0ulm3+EiMnKqihNfbTnMsg0HAYiNCKRtfFj1ppiRYf4+/fBx6FgpC7/NYs2OXAD6dWrKyD4JNIsM8llM5+PcsgjcTvx6qCtCLp69w2Acm9JwbEwjYNgvfB0OAJ2SIrlhUGs+WpFJemwwo/u19HVIIiJep2KEiIhckhPFlfzn8ww2ZOQTHxPMLyd1qXc/Ma9P/GwW2ic2oX1iEwBcbg9ZucWnNsU8yfpd+azcfASAiFA/Uqo3xQyneWRgnRQnMg+fJH11Fhv3HMNuMzOkRwuG944nItS/1ue+VJ7yIhzbl57qimjm63CkATLZA7B3vBbHxjTcJw5jadLc1yEBMKJ3Atm5JXz65T7iY4Lp0jrK1yGJiHiVihEiInJRPIbBys2H+WhFJi63hxsGtWZYr/hGf4KEt1ktVRtdtm4exsg+VXk9lF9a3TmxM+sE357qTAgOsNGmRdWmmCkJ4cTHBGMxeyffhmGw48AJFqw+wK7sQoL8rYzr35Jre7ZoEPt9OLcsApcTu07QkMtg6zwMx9bFODYvIGDQPb4OB6jam+aOke04cqyUNz7bwRNTU2kaEejrsEREvEbFCBERqbEjBaW8tWg3GTmFtEsIZ+rIdsQ20ZtjbzCbTMTHBBMfE8y1PVtgGAZ5heVkZBdW7zuxcU/ViR1+dgtt4sKq951o1SwEm/XilsZ4PAbfZeSz4Nssso4WEx5s5+YhyQzs1hx/e8N4e+CpKMaxfRnW5D5YwuvHT7OlYTL7h2BrNxDn9uV4ek7AHFI/uhD8bBYemlS1oeVLn2zh8dtTCfBrGH8+RUQuRH+biYjIBbncHhauyWb+qgPYrWbuHNmOAV2aaVO1WmQymYhtEkhsk0Cu7lr1QftEcWV150TGwULmrNwHVHVZJDULISUhnJQW4bSOCzvnBxaX28PqbUdZuCabo8fLiG0SwB0j29GvY1Ns1obV3VLVFeHArhM0xAvsXUbg3LEcx5aF+Pef4utwqkWFBfDz6zvxj/c3MSNtBw9O7Ozzo3RFRLxBxQgRETmvfYeLmL1wJwfzS+nVLoZbh7YhLNjP12FdkZqE+NGnQyx9OsQCUFLuZM+promMnJOkr84mzcjCZIKE2JCqZR3x4bRpEUZIpYsl63JYvDabE8WVJMQG8/PrO9EzJRqzueF9sPFUFOPYthRr6z71Zo2/NGzm4Ehsba7CuWsl9h7jMQfUnz1w2ic24eZrk/nv0j3MX3WA8QN8f+qHiMjlUjFCRETOqsLh4tOV+1i2/iDhIX78clIXurWpH63LUiU4wEb3NtF0bxMNVP2eZR764cSOFRsPsWRdDlC1tKPS4aZtfDh3jmxHx1YRDbqzxbllcVVXhE7QEC+ydx2Fc/fXOLcuwa/3Db4O5zRDe7Yg+2gx877eT3xMMD1Son0dkojIZVExQkREzrAls4B3Fu/ieFElg3vEMWlga61TbgD87VY6toqgY6sIAJwuDweOVhUnSh0eeiRHkhwX5uMoL59RUXLqBI3e6ooQrzKHN8OalIpj+zLs3UZhstefPXFMJhO3j2jL4YJS/p22g8dvTyUuqn4etysiUhMNa3GoiIjUqqIyB//6bDsvfrQZu83CY7f14LZhbVWIaKBsVjNtWoQzul9LHryha6MoRAA4tiwCZ6W6IqRW2LuNAWc5jh3LfR3KGWxWCw9O6IyfzcJLn2yhrMLp65BERC6Z3l2KiAiGYbB6+1HeX7aX8koX4we0YlTfxAa3oaE0ftVdEUm9sDSJ83U40ghZohKxxHfGuXUJ9k7DMFnr1xG3EaH+PDihE3/9z0be+GwHv7qhS4Pc96U2eTwGFQ43FQ4XlU73qV9XfV3hcFP5k68rHO6q6yqrvg4IsHHHiLaENoDjjUUaMhUjRESucPmF5by9aBfbD5ygdVwod4xsr9ZfqbccWxef6ooY7+tQpBGzdxtD+fw/49y9EnvHob4O5wxtWoQz+boU3l68mzlf7WPSwNa+DumyuNyeM4sDP/m6urBQeepr56nHfvz8qV87XJ4az+1ns+Bnt+Bvt+Bvq/r/lj35pIX6cevQlFp81SKiYoSIyBXK7fGwdP1B5ny1D7PJxG3DUhjUPU5Hxkm9ZVSU4Nj2eVVXRIS6IqT2WJqmYI5NxrF5Ibb2gzCZ699b5kHd48jKLWbB6iziY4IZHR1SJ/MahoHD5TlVMPhxseAnxQHn2TsRKh1ndiq4PUaN5jaZqvbG8T9VPPA7VTyIDPX/4TG7pfqaH4oMp+7x+/4ea/X9Z+sq+e/yvazYkMOwXvFEhQV4O4Uickr9+5tVRERqXXZuMW8u3EXW0WK6JUdx27AUIkL9fR2WyHlVdUVUaK8IqXUmkwm/7mMoX/Qirr1rsKX093VIZ3Xr0BQO5ZcyK30nHZKjCbadubTOYxhnLEv4oWBwqphQeWqZwjmKBdXLGE59bdSsdoDVYsLfbq0qAPj90HkQHuxXXSj4cfHA32bB389aXWT44T8rfnYLdqu5Tk4B+tmwdqzYcJB5X+9n2ugOtT6fyJVKxQgRkSuIw+lm3qr9LF6TQ3CgjZ9f34nUttEN+ohHuTKc3hXRwtfhyBXAEt8Vc0Q8jk0LsLbph8lU//bQsVnNPDChE9Nnr+PJf60mJsz/R10JVcUDh7PmSxbsNnNVYcD2Q6EgJNBOdPiPugzsp3cW/LhT4afFBaul/uWsJqKbBDCkRxyfr89hRJ9ELV0UqSUqRoiIXCF2HjjOW4t3k3einKu7NOOmIckE+dt8HZZIjTi2LVFXhNQpk8mEvdtoKpa/juvARmytevo6pLMKD/bjF5O6MG/VARwOFxGnliz4nbaUwfqjzgTrOQsL2gjzB6P7JbJy82HmrNzHQxM7+zockUZJxQgRkUautMLJB8v38vWWI8SEB/DbW7rRvmWEr8MSqTGjshTH1s+xtkrFEhHv63DkCmJN6oVp/ac4NqVhbdmj3naRtWoWynM/709+frGvQ2k0QgLtjOidwNyv95N5+CStmzeOo5FF6pOG2TslIiIXZBgGa3fm8od/r+GbrUcZ1TeR6dN6qxAhDY5j6xJwlmPvqRM0pG6ZzBbsXUfhyd+PPvghRQAAIABJREFU+9AOX4cjdey6XvGEBP5/9u47Poo6/+P4a2Z3Z0tCAiSEDqH3UEKTXkIJLYBY76feKXfWOwt6Ytc78e48G+rdKaced+p5FlRqaNJ7T+i995q2ZXZ35vdHEEUJBEh2Uj7Px8NHki2zb9Zkd/Yzn/l8HXy9cI/VUYQok6QYIYQQZdCZbD/vTNrIe5M3U6mCk+d/2Z5RvRqgOWxWRxPiquR3RcyWrghhGUfjriieiugbplkdRUSY22ln8A2JbN1/ls37zlgdR4gyR4oRQghRhhimyXdrD/HsByvZsu8Mt/RpyLN3JlOnamSWfBOiqF3oimgnXRHCGorNgZY0kPCRrYRP7LY6joiw3m1rEBfjZNKC3ZiFXUZECFEoUowQQogy4vCpPP78yTo+nbODBjVi+MPoTgzoWAebKi/1onQyA3nom2ZjT0zGFiddEcI6jma9wBmFvl66I8obh93GsG712Hcsh7XbT1odR4gyRQZYCiFEKRcMGUxfvo/py/fj0myMHtKMG1pUK7GD1oQoLH3THNBlVoSwnuJwobVIQV83mfCZQ7K8bDnTpWU1Zq48wNeL9tC2cbwU+YUoIvKXJIQQpdiuQ1m8+K9VTFm6jw7NEhj3m850aVldChGi1MufFTHrfFdEHavjCIHWsh/YnegbplsdRUSYTVUZ2aM+x854WbbxmNVxhCgzpBghhBClkC8Q4uPZ2/nTJ2vRg2Eeuak1vxnaghiPZnU0IYqEvmlufldEu2FWRxECAMUVjaNZL0K7V2JkS7t+edOucRXqVa/At0v2EgyFrY4jRJlQIooRCxYsYMSIEQwdOpT/+7//4+DBg1ZHEkKIEmv9zpM8+8FKFqw7TN/2tfjj6E4kNYizOpYQReaHroh22OLrWh1HiAu0pIGgqOiZ6VZHERGmKAo39mzA2ZwA89cdtjqOEGWC5cWIrKwsnnzySd544w2mTp3KTTfdxIsvvmh1LCGEKHGycgP8/dtNvDNpI1EuO0/fmcztKY1xaTL+R5Qt+V0RXllBQ5Q4alQlHI27Ety+CMN7zuo4IsKaJ1ameWIlpi3fjy8QsjqOEKXeZfdgQ6EQ8+bNY8GCBWzbto2cnBwqVKhA06ZN6dGjBykpKdjt17cTvH//fuLj46lXrx4APXv25Pe//z1nzpyhcuXK17VtIYQoC0zTZEnmUT6ftws9ZDCyR30GdqqD3WZ5PVmIImfq3vyuiLptpStClEha60EEty8iuHE2zk43Wx1HRNiNPRvwx3+vYdaqAwzvXt/qOEKUagVWEj777DPef/99GjRoQIcOHejduzdRUVHk5eWxe/duvvzyS/785z9z7733ctttt11zgHr16nHq1CkyMzNJSkpi6tSpABw9elSKEUKIcu/4GS//nrmNbQfO0bh2Re4a2ITqcVFWxxKi2OSvoOGVFTREiaXGVsVevyP6lnlobQajOOU1uTypVz2G5MZVmLX6IH2Sa8msJiGug2KapnmpK/7yl79w9913U6VKlQLvfOLECf71r3/x5JNPXleIZcuW8c477xAIBOjRoweffvopH3/8MU2bNr2u7QohRGkVCht8s2AX/5u9HYdd5VdDW9CvY11UVVbJEGWX4c/jwN8ewFW7GdVuHmt1HCEKFDi+j8MfjKFSz9uo1G2U1XFEhB08nsNDf53HkO71+XVaK6vjCFFqFViMsMqpU6fo3bs3K1euxOPxFOo+p0/nYhgl6p9xWVWqVODkyRyrY5QJ8lwWHXkui871Ppd7j2YzMX0bB0/kkty4Crf3a0ylCs4iTFh6yO9l0SkNz2Vg3RT0NV/jGfEitiqJVscpUGl4LkuL0vxceme+iXFiD1G3vYbisP41ujQ/lyVNYZ7Lj6ZvZcWWY/zpNzcQF+uKULLSR34vi05pfC5VVSEuLrrg669mY6FQiM8//5w//OEP/Otf/yIvL++6AwKcPJm/PJJhGLzxxhvceuuthS5ECCFEWRHQw/zvu528/J81ZHt1HhzRigdHtiq3hQhRvpi6D33jLGx12pToQoQQ39PaDMH05xDcttDqKMICad3y591NXrLX4iRClF5XNX3ylVdeQdd1WrVqxapVq1i2bBn//Oc/rzvEW2+9xbp16wgGg3Tt2pXHH3/8urcphBClyaa9p/nPzO2cyvLTq00NRvVqgMflsDqWEBGjb5oDgTycycOtjiJEodirNcJWvQl65kwczfug2GRlo7LA8GWTvXYpZo0OKPaC50HExbro3bYWc9ceZGCnOtSIl9khQlyty75qTpw4kTvvvBNVzW+g2LFjB5988gkAI0eO5IYbbiiSEOPGjSuS7Qghrp6Rexo9Ywb7D2zAQM1/47VrP3y1ff+z8+LL7T+93AF258WX2xznf3aCakNRZN7BT+V4df733S6Wbz5Gtcoexv6iHY1rV7Q6lhAR9UNXRGvpihClitZmML70NwjtWo6jSXer44jrFD57GN/MN8nLOYU9cR2ulAdR1IIbyQd3qcuizCN8s3gPD46Q2RFCXK3LFiMCgQC33347Y8eOpU2bNiQnJzN69GhatGjBunXr6NGjR6RyCiGKmJF1DH3DdII7loECUY07EggrENIxQzqEApj+PMzQWcxQ4IfLwzoY4at/QEW9RDHjfPHC5rhMsUO7uMhhK+Dy819R7aWi6GGaJiu3HOe/c3fiC4QY0iWRoV3q4rDbrI4mRMTpm+dKV4QolWy1WqHG1SWwYTr2Rl0v+8FVlGyhw1vwzXkHxeYgpuMQsldNI7DkPzi731XgfkWMR2NAh9pMWbqPvUezqVc9JsKphSjdLluMuPfeexk0aBDjxo2jcuXKPPHEE2RmZrJjxw5uv/12+vfvH6mcQogiEj59EH39VEJ7V4Nqx9G8N1rrVKrWSyz0UBzTCEEoeHGR4qKv5y8PB/OLGhddH8AM/eTygBfTe+5n97+2ooeSX6SwOa7Q0aH96HY/L2pcsthh+1HRw+a45qLHqSwf/5m1nU17zlC/Rgy/HNiUWgkFD/cRoiwzdR965szzXRH1rI4jxFVRFAWt7WD8c/9OaN9aHPU7WB1JXIPgjiX4F/4LtWJV3AMfJb5+ffw66Bumobgr4OxwY4H3HdCxDvPWHWbSwt08fmvbCKYWovS74slttWvX5r333mPu3Ln86le/4rbbbuPXv/51JLIJIYpQ+MRuAuumEj6wARwutKRUHK0GoHpir3pbimoHzY6iuYsh6Q9MI3yJYkeggCLHj4sd+kWdHBd+1r8velx8f4zQNaRTCjxt5ajbjR4mv9Bhs4PqQLHZMVU7B0762HIwh9rY6N+qCo3qhFFOryF4zg6qPb/IYcv/is2e/1xfuOz89+qPr5dOClG66Zu/y++KaJdmdRQhrok9sT1KbDX09dOw12tfKrrzRD7TNNHXfoO+bgq2ms1xpzyI4syf/aB1uBHTl42+fiqKOwatZb9LbsPttDPkhrr8b94utuw7Q/PEypH8JwhRql22GJGXl8cXX3zBwYMHadiwIRMnTmTChAncfvvtPPfcczRr1ixSOYUQ18A0TcJHt6Gvn0r48BZwRqG1H4HWIuXCmy2A1x9kxrK95OUGcDpsODXbxV8dKk7NjtOhojlsqBHa0VJUG2juyBU9rrXI8ZMOEUP3YfoDmEYQMxyCcIhwUCeo61QxQ6Q4jfwHPgz64esMryigni9MXFTEOF8IsdkvFEUuKmKcL5L8+PqC7/fzy74vsFwokNh+VEyRHXFRSKbuI5g5E1vtJGwJ9a2OI8Q1UVQVZ+tB+Bd9RPjQJuy1ZXZAaWCGg/gXfkRo13Lsjbvj6n7XRUNIFUXB2f0uzEAugWWforgq4GjY+ZLb6t2uJrPXHGTSwt00q1tJ3geFKKTLFiMeeeQRoqOj6dSpEytXrmT79u289NJLbN++nZdffpnGjRvz3HPPRSqrEKKQTNMkfDCDwPppGMd3obhjcXa+BUez3iiOi9fC1oNh3voyk12Hswq9fc2h4nLY0M4XLL7/3vWzIkZB36u4NHv+dn5U5LDbrDnX9kLRg6Ipevx4HehgKMzUZftIX3EAj8vObSmN6Ng0AcU0IBzMP+UlHMr//vxXjNAP34dD+UWS87czL1wWAiN40WWEQ5jGj77/8f2C/gvbNH+yLcIhMK/hlJiCqLYfdXB8X6z4SUFDLbi48cNldrKrVsOsniwdIGWUvuU7zECuzIoQpZ69UReUtd+ib5gmxYhSwPTn4pvzDuGj29Haj0RrO/SSBQRFteHqcx++9Nfxz/8nijPqkv9/HXYbaV3r8a/0bazbcZLkJgmR+GcIUepdthixYcMGVq5ciaqqjBw5klGjRgHQpEkTPv74YyZNmhSRkEKIwjENg9DeNegbpmKcPogSHYez2504Gne75PJUhmnyz2lb2H04i8d/kUz1ii70YBi/HiYQPP/fFb736+H8+wTD5HiDBIIhAkGDQDCMrocxryK/3ab8vIBRUEHj/FeXZkNzqPnfO2xo54sjP76Nw65acpRi+4GzTJy5neNnvHRtWY1b+jYi2v39cp1q/gfviKe6NNMwzhcugpcsblxUHPlpweN8YeT7LpALhRXj4iLLRZcF/eAPXdQ98sNtzm8TOAXY67bF1ff+yy6xJkofM+gnmCFdEaJsUGx2tKSBBJb/l9CxndirNbI6kiiAkX0Cb/obmDmncPW5r8Buh+8pdg33gIfxTv0Tvjnv4hnye2wJDX52uy6tqjFz1QG+XrSHto2qoKol5R1eiJLrssWIbt268cQTT9CpUydWrFhBz549L7r+xhsLHuYihIgc0wgR2rkcfcN0jKxjqLHVcPUajb1h5/yj0wX4Yt4u1m4/yS19GtKzXa1CD7AsdC7TRA8ZPxQxvi9gnC9U/Ph7/08LHnr4QlEjK1f/WREkbBS+zKEoFFzM+ElXx4+7NX5+usrPCyWX2tnI9QWZmL6NRRlHiI91MeaWNrSoV7LPIVVUFdTzcy+sDkP+7w5GGOehFZye9SG+Ga/hHvDwRacXidJN3/x9V4TMihBlg6NpT/R1U/K7IwY+anUccQnh47vwzRqPaRq4Bz+BvXqTQt1P0Ty4U8fgnTwOX/qbuIc9ja1SjYtuY1NVRnSvz9+/3cSyTcfollS9OP4JQpQply1GvPbaa8yePZtDhw6Rlpb2s2KEEMJaZkgnuH0xesYMzNzTqHF1cKU8kD9M6wrLi81Zc5DZqw/SN7kW/TvULpZ8iqJc+NBe1EJh40JXxkUdGvolujiCYQK68UPXxvnrvP4Q53ICF3WCBEPGVeXQ7OpPihk2zuYEyMoLMLBjHdK61cOpySkGV0tRFLDZiW2fSl5Ywz9vAt4pf8I9aAxqVCWr44nrZAb952dFtLrkEUYhSiPF4cTRqj/6mq8Jnz6ILa543lvFtQnuWYV//gSUqMpEDXwMtWK1q7q/6qmIZ/ATeCe/jG/Ga3jSnkGNjrvoNslNqpBYrQKTl+yhU/OqOOyy1KsQl3PZYoTNZiM1NTVSWYQQhWQG/QS3zEfPnInpy0Kt2hBXtzux1U4q1OkI63ac5H9zd9K2UTy39W1UKgct2W0q0W4VLpz2UDQMw/xJEePSp6UEggZ+PYQeNPK7On5U0Eio7GFAh1okVpP1xouCo35HFGc0vtlv4538Mp5Bj6NWlCNOpZm+eR6mP0dW0BBljtaiL3rGDPQN03H3vc/qOILzXZoZ6eirvkCt2hD3gIdRXRWuaVtqTEJ+h8TUP+Ob8TqeYU+juH5YmltRFG7s2YDXP9/AgvWH6VdMB3uEKCsKLEY89NBD/OY3vyEpKanAO2dmZjJhwgTefffdYgknhLiY6c9F3/wd+qbZEMjDVrMFWtv7sFVvWuiCwu7DWbw/ZTOJ1WP4zbAWck7jT6iqgttpx+284srHBfrxAEtRNOw1m+MZOhZf+ht4J4/DnfqYzBkopcxggGBmOrZaLbFVbWh1HCGKlOKMQmveBz0zHaP9CNTYqlZHKtdMI0RgyScEty3AXr8jrl6jr3v+kC2+Lu4Bv8OX/jremW/iGfx7FIfzwvXNEyvRrG4lpi7bR7ek6te1PyFEWVfgX8ctt9zCSy+9RG5uLh07dqRevXpERUWRl5fHvn37WLlyJTExMTzyyCORzCtEuWR4swhunIW+ZR4E/djrtkVrO/SqP4ydOOtl/FeZVIzWeHhUUrGcPiFEcbHFJ+IZ9gzeGa/hnfYX3P1/i71WS6tjiasU3PJdfleErKAhyihHq/7om2ajZ6Tj6vFLq+OUW6buwzf3b4QPbUJrMwStw0gUpWhOm7DXaIarz/34576Lb+67+TONzs/oUhSFkT3rM+4/a5mz+iDDutUrkscUoiwqsBjRvXt3unfvzsaNG1m0aBEZGRnk5OQQExNDkyZNePPNN2nevHkkswpR7hi5p9EzZhDctgiMEPb6ndDaDsZW+erb/nK8Om9+kYFpmjx6cxtiomRlAlH6qLFV8aQ9gy/9dXzpb+LqPRpHwxusjiUKyQwG0DOkK0KUbaqnIo4mPQhuW4SWnCZzbixg5J7GN/NNjLNHcPb4FVrTop9756iXjNntLgKLJ+Jf8CGu3r++UOxoUCOWdo2rMHPVAXq3q0kFj+xzCXEpV+wbatWqFa1ayXrJQkSSkXUMfcN0gjuWgQKORl3R2gxCjb26YUvf04Nh3pm0kdPZAZ64rQ3VKnuKOLEQkaN6KuIZ+hS+WePxz3sf05eD1qq/1bFEIQS3yKwIUT5oSakEty5A3zgLV+dbrY5TroRP7cM38y3MYAB36mPF2kGnNeuF6c9BXz2JgKsCzhtuu3Da7Ige9Vm/8yTTl+/n1r6y1KsQlyInMQlRgoRPH0RfP5XQ3tWg2nE0743WOvVn05qvhmGa/HPaFnYfzuL+4S1pVKtiESYWwhrfL7Pmn/c+geX/xfRloXUYVSqHsZYXZjCAnpmOrWYLbNVkx1yUbWpMFewNOhHcMh9nmyEXDTkUxSe0fwO+7/6B4ozCk/YMtsq1iv0xtTZDMH3ZBDfNRvHE4GwzBICa8VF0aVmNeesO079DbSrHuIo9ixCljRQjhCgBwid2E1g3lfCBDeBwoSWl4mg1ANUTe93b/nL+LtZuP8ktfRrSvmlCEaQVomRQ7BqulAcJLP0P+obpmL5snN1/iaLKLJSSKLh1HqYvG01mRYhyQmszmNCu5eib58qMlAjQN80lsPxT1Lg6uAc+iuqJzMEXRVFw3nBbfofEqq9QXBUunBaS1q0eK7ccZ/KSvfxqULOI5BGiNJFihBAWMU2T8NFt6OunEj68BZxRaO1HoLVIQXFGFcljzF1zkFmrDtI3uRb9ZXkpUQYpqoqz210o7lj0dZMxfDm4U+5HsTuvfGcRMWbo/KyImi2wS1eEKCdslWthr9sWfdMctKSBKA45Ml4cTMMgsOJ/BDfNxlanDe6+91+0ukUkKIqKq+dofP5cAosnoriicSQmEx/rplebmny37hADO9WhelzR7N8JUVYUzUhZIUShmaZJ6MAGvFPG4Zv2F4wzh3F2voXo21/H2S6tyAoR63ec5LO5O2nbKJ7b+jaS9nVRZimKgrP9CJxd7yB8IAPf9NcwA3lWxxI/Etwy/3xXhMyKEOWL1mYwBPIIbl1gdZQyyQwG8M99l+Cm2Tha9sPd/3cRL0R8T7HZcff7LWqVevi/+wehI9sAGNIlEc1u45tFeyzJJURJVqjOiOXLl1/yck3TqFatGjVr1izSUEKURaZhENq7Bn3DVIzTB1Gi43B2uxNH427Xveb1T+0+ksX7UzaTWD2G3wxrgapKIUKUfVqLvijuCvjnTcA75U+4B42RKfYlQH5XxAxsNZtjr9bY6jhCRJStakNsNZqhZ87E0aIvis1hdaQyw/CewzdrPMbJfTi7/AKtZT+rI6E4nHgGPoZ3yiv4Zo3HM+wpYuLq0L9DbaYu28feo9nUqx5jdUwhSoxCFSOeeeYZTpw4AUDFihU5d+4cAHFxcZw6dYomTZrwxhtvkJiYWGxBhSitTCNEaOdy9A3TMbKOocZWw9VrNPaGnS+sSV2UTpz18vZXmcREaTw8KgmnQ86fF+WHo35HFGc0vtlv4538Mu5BY7BVrGF1rHItuGVBfleErKAhyimtzRB8M/5KcMdStGa9rI5TJoTPHMY38w1Mfw7u/r/DntjW6kgXKK5o3IPG4J08Dt+M1/CkPcuAjnWYv/4wXy/czZhbS05WIaxWqNM0Ro0axR133MGaNWtYsmQJa9as4a677uLWW29l9erVtGzZkpdeeqm4swpRqpghHX3zd+T970n8Cz8Eu4Yr5QE8N72S3w1RDIWIHK/Om19kYBgmj97cmpgoWddalD/2ms3xDB0L4SC+ya8QPiGtsVYxQ3p+V0SNZtirN7E6jhCWsNVsjlqlHnrGDEwjbHWcUi90eAveKS9DOIRn6FMlqhDxPTU6DvegxzGNMN4Zr+EychnUuS6b951l6/6zVscTosQoVDHiP//5D2PGjMHlyh+843K5eOSRR/j3v/+Nx+Nh7NixbNq0qViDClFamEE/ekY6eZ89QWDpxyhRlXAPfBTPyJfyj9qqxTOqRQ+GeWfSRk5nB/jtjUkyJEmUa7b4RDzDngHNjXfaXwgd3Gh1pHIpuHV+/rKrspKAKMcURUFrMxgz+wShPautjlOqBbcvxjfjddSoyniGP4etSj2rIxXIVqkGnoGPYnrP4Ut/g94tK1GpgpNJC3djmqbV8YQoEQr1qcjj8bBx48U7cps3b8btdudvpJg+XAlRmpj+XAJrJ5P73zEEVn6OWrkW7iFP4hn2DPY6rYt1gKRhmnwwbQu7Dmfx66HNaVw7MstZCVGSqbFV8aQ9gxqbgG/mWwR3LrM6UrlihnT0DdIVIQSAPbEdasXq+csQywfRq2aaJoHVk/Av/BBbjab5r+0V4q2OdUW2qg1x93sI48xhwvP+xvAutdhzJJv1O09ZHU2IEqFQfeK/+93vuPvuu+nTpw/Vq1fn2LFjzJ8/n+eeew7IH3A5YMCAYg0qRElleLMIbpyFvmUeBP3Y67ZFazsUW0L9iGX4cv4u1mw/yc29G9KhaULEHleIkk71VMQz9Cl8s97GP38Cpj8HrZW8X0VCcOuC/K6IvvdbHUUIyymKitZmMP4FHxA+mIG9ThurI5UaZjiIf+GHhHatwNGkB87udxbLqa7FxV47CVfv0fjnvU+yNpn0yu35etEe2jSMlwHjotwr1F/y8OHDadmyJbNmzeLEiRMkJiby+eef07BhQwB69+5N7969izWoECWNkXsaPWMGwW2LwAhhr98Rre0QbJVrRzTHd2sPMWvVQfq2q8WAjpF9bCFKA0Xz4E59DP+89wks/yx/mGKHUbLcbTG6MCuielPsNZpaHUeIEsHesDPKmm8IrJ+GrXbxdkyWFaY/F9/stwkf24HWYRRam8Gl8nlzNLwB05dDYPl/ub+anRe2NGH55mN0bVXd6mhCWKrQZcWGDRteKD4IUZ4ZWcfQN0wnuGMZKOBo1BWtzSDU2GoRz7J+x0n+O3cHbRrGc1tKo1L5Bi1EJCh2DVfKgwSW/id/ZRtvNq4ev0RRZbWZ4hDcthDTew6tz71WRxGixFBUO1pSKoFlnxA+tkNOX7oCI+s43plvYOaextXnPhwNO1sd6bporfpj+rKpuGEat8WH+Xaxm47NquKwy+nuovwqVDHi3LlzfPTRR2zduhWv13vRdZ9++mmxBBOipAmfPoi+fiqhvatBteNo3hutdSpqdJwlefYcyeb9KZtJrBbDvWktpNVPiCtQVBVnt7tQ3LHo6ybj8+fgTrkfxe60OlqZkj8rYjq26k2w12hmdRwhShRH0x7o66egb5gmxYjLCB3biX/WeADcg5/EXq2RxYmKhtbhRkx/Np23LeJwQGXBhtr0ay9draL8KlQxYsyYMei6Tmpq6oWhlUKUF+ETuwmsm0r4wAZwuNCSUnG0GoDqibUs04lzPsZ/lUFMlMbDo5JwOuTorhCFoSgKzvYjUDyxBJZ8jG/6a7gHPoLilNVniop0RQhRMMWu4WjZH331V4RP7ccWX9fqSCVOcPdK/Av+iRIdh2fgo5Z0nhYXRVFwdrsLw5/LjftW88WKKPxJ/4dLKz0zMIQoSoX6zV+/fj0rVqxA07TiziNEiWCaJuGj29DXTyV8eAs4o9Daj0BrkWL5h5ZcX5A3v8jAMEwevbk1MVHydynE1dKa90FxVcA/7328U17BPehx1KhKVscq9aQrQogr01r0Qd8wHX3DNNwpD1odp8QwTTP/eVn9FbZqjXH3/x2KK9rqWEVOUW24+9zHmW9f5cbTC1k7ryZdB/azOpYQlijUSUpNmjTh2LFjxZ1FCMuZpknowAa8U8bhm/YXjDOHcXa+hejbX8fZLs3yQkQwFObtSZmczvLz2xuTqB4nR3OFuFaO+h1wpz6GkXsa7+SXCZ87YnWkUi+4bVF+V0TycKujCFFiKZoHrUVfQnvWYJyT/WsA0wgRWPQv9NVfYW/QGfegx8tkIeJ7il2j8rDHyLLH03T/5+Qc2G51JCEsUajOiM6dOzN69GhGjhxJfPzFa/qOGjWqWIIJEUmmYRDauwZ9w1SM0wdRouNwdrsTR+NuKPaS0XlgmCb/nLaVXYeyuC+tBY1rV7Q6khClnr1m8/ylP9Nfxzf5Fdypj0V0Wd6yJL8rYhq2ao2xVZcVNIS4HEer/ugbZ6FnTMfV8x6r41jK1L345vyN8OHNaG2HorUfgaKU/aGOiubB0f9Rsqe9Qszstwjf+By2SjWsjiVERBWqGLFmzRqqVq3K0qVLL7pcURQpRohSzTRChHYuz5+un3UMNbYarl6j85ffKmFrWH81fzdrtp3g5t4N6disqtVxhCgzbPF18Qx7Bu+M1/BO+zPufg9hr51kdaxSJ7j9fFdE79/Iyj5CXIHqjsHRtAfBrQvQkodbNgzbakbuaXzpb2KcO4ohwpVIAAAgAElEQVSrx904mvawOlJE1ahdg8+q30aPYx+TN/2vRA9/ttz+LojyqVCftj7++OPiziFERJkhneD2xegZMzBzT6PG1cGV8gD2xPYoasmrxn+39hAzVx2gT7uaDOgoU5eFKGpqbFU8ac/gS38D38zxuHrdg6NRF6tjlRpmOJg/K6JaY2wyK0KIQtGSUgluWYCeORNXl19YHSfiwif34Zv5JmZIx536GPZaLayOZIl+vdrxzofHeNg2G9+M1/EMe7pMn6IixI8V+KnLNM0L3xuGUeB/QpQmZtCPnpFO3mdPEFj6MUpUJdwDH8Uz8iUc9TuWyELE+h0n+e/cHbRpGM/tKY3liKMQxUT1VMQzdCy2ao3wz5+AvnGW1ZFKjeC2RZh5Z9GSh8trlBCFpFaIx96oM8FtCzF82VbHiajQ/vV4p74CNjuetGfLbSECIL6im8ZJrXg/uxfh7BN4Z76BGQxYHUuIiCiwMyI5OZl169YB0Lx585/tXJimiaIobN26tXgTClEETH8u+ubv0DfNhkAetpot0Nreh6160xK947znSDbvT9lMYrUK3DusBapacrMKURYomgd36mP4508gsPwzTG8WWsebSvTrhNUudEVUbSRdEUJcJa31YEI7lhHcNAdnhxutjhMR+qY5BJb/FzU+EfeAh1E9MgNrSJdExmYeZVGFwfQ8OQXf3HdxD3i4xJ0yLERRK/A3fPr06Re+/+677yISRoiiZnizCG6chb5lHgT92Ou2RWs7tFQMqDtxzsf4rzKIidL43ajWODWb1ZGEKBcUu4ar7wMEln6MnjEDw5eDq8cvUVT5G7yU4PbFmHln0HreI0UbIa6SrVIN7Int0Dd/h9Z6EIrmtjpSsTENg8CKzwhumoO9bltcfe5DcTitjlUixEZp9OtQm6+XhWnf+1aiMj7Dv+BDXL1/XS6GeYryq8BiRPXq1S987/P5aNiw4c9us3jxYmrWrHndIebPn8/48eMxTRPTNHnooYfo37//dW9XlF9G7mn0jBkEty0CI4S9fke0tkOwVS4d8xZyfUHe+iIDwzB59ObWxEaVjBU9hCgvFFXF2e1OFE8s+tpv8fmzcac8gGKXHecfM8NB9PXTUKs2xFazudVxhCiVtLZDCO1bS3DrfLTWg6yOUyzMYAD/vPcI7V+Po2V/nJ1vLZGnxlppYMc6zF93iP/uq8yDHUahr/6KgCsa5w23S6FXlFmF6v259957mThxIrVr//BBbt68eTz//PMsWbLkugKYpsnvf/97Pv30Uxo3bsy2bdu47bbbSElJQZUXKXGVjKxj6BumE9yxDBRwNOqK1mYQamw1q6MVWjAU5p1JmZzK8vP4rW2oHhdldSQhyiVFUXAmD0dxxxBY8jG+6a/lt83KYLELvu+KcPW8W3aWhbhGtir1sNVsgZ45C0eLlBKzpHhRMbzn8M18C+P0fpxd/g+tZYrVkUokj8vO4BsS+WL+LvZ26kJiy2yCm2ajuGNxth1idTwhikWhPu3//ve/Z/To0Zw4cQKA2bNn8/zzz/Pee+8VTQhVJScnB4CcnBwSEhKkECGuSvj0QXxz/07eF08R3LUCR/PeRN36Kq6ed5eqQoRhmnwwbSs7D2UxekgzGteW8yiFsJrWvA+ulAcIn9yLd+qfMHLPWB2pRLi4K6L8Dp8ToihobYdg+rII7ri+g3wlTfjMIbzf/hHj3BHc/X8nhYgr6NOuJpUqOJm0aA9a51uwN7wBffVX6NsWWh1NiGJRqM6IAQMGkJuby913383tt9/O3//+dz744AOaNm163QEUReGtt97igQcewOPxkJeXx4QJE657u6J88B/egXfe54QPbACHCy0pFUerAaieWKujXZOvFuxm9bYT3Ny7IR2bVbU6jhDiPEf9DiiuaHyzxuOdMg73oDHYKtawOpalgtuXSFeEEEXEVr0pakJ99Ix0HE17lokZNaFDm/DN+RuKw4ln2NPY4hOtjlTiaQ4bQ7sm8p+Z28nYfYY2Pe/BF8glsHgiiisaR2Ky1RGFKFKK+eM1PH/kUst2Tpw4kY8++ogPP/yQRo0aAVx3B0MoFGL06NH89re/JTk5mbVr1zJmzBimT59OVJS0p4tLM8NBTs/+F9nrZqG6o4ntMISY9qnY3KW3fXr6kj28981GBnVJ5L6RSbJzL0QJFDi2h2P/G4dphKl2y9O4aja2OpIlzHCQg39/CFuFOGrcNU5er4QoAnk7VnP8yz9TJe1hKrTsYXWc65K9YS6n0iegxdek2s1PY4+tYnWkUiMUNnjw1Xk47Crjx/RGCQU4+umL6Mf3Ue2253DXlU40UXYUWIxo2vTnSx5+f1NFUYpsac+NGzfy5JNPMmPGjAuXpaam8pe//IWkpKRCbeP06VwM45L/jBKpSpUKnDyZY3WMUsvwZuGf+zfCx3YQ22kY4eaDUBwuq2Ndl/U7T/Lu1xtp3SCeB0e2xGbBaUrye1l05LksOiXxuTSyT+Cd/ldMXxbufg9hr1249yqrFeVzqW9dQGDxRNypY7DXblUk2yxNSuLvZWklz+UPTNPA+9VzAHhG/fGqV1EoCc+laRroq79G3zANW62WuFMeLJUrhFj9XK7aepz3Jm9m9JBmdGlZHdOfi3fKKxh5Z/EMHYstvq5l2a6W1c9lWVIan0tVVYiLK/hgcYGnaURqOc9q1apx7Ngx9uzZQ/369dm9ezenT5+mTp06EXl8UbqET+7FN/sdTH8urj73EXdDv1L3R/lTe49m8/7kzdStWoF7h7WwpBAhhCg8NSYBT9qz+NJfxzdzPK5e9+Bo1MXqWBFjhkPo66eiJjTAVqul1XGEKDMURUVrMxj//AmE92dgT2xrdaSrYoZ0/As+ILRnFY6mPXF2uwNFLdQZ4eIn2jdNoM6K/Xy7eC8dm1XF7orGPWgM3snj8KW/jiftWdSYBKtjCnHdCnyFuNSSnYZhcOrUKeLj44tswGSVKlV48cUXefjhhy90YrzyyitUrCiD+8TFgjuW4l88EcUdgyftmVJVFS7IiXM+xn+ZQUyUxsM3tcaplf5zRIUoD1RPLJ6hT+Gb/Tb++RMwfTloSQOsjhURwR1LMHNP4+p+l5yeIUQRszfohLLmGwIbpmKr26bU/I0Z/hz8s94mfHwnWseb0FoPKjXZSyJVUbixZwPe/CKDhRuO0De5Fmp0HO5Bj+OdMg7v9L/iSXsG1SOfl0TpVqhyZW5uLn/4wx+YMWMGoVAIu93O4MGDefbZZ6lQocJ1hxg2bBjDhg277u2Issk0wgRWfkFw4yxs1ZviSnkA1R1jdazrlusL8tYXGYQNk0dvbk1sVNlaykuIsk7R3LgHPop//gQCKz7D9GWhdbypTO+A/9AVUR9brfJ3eoYQxU1RbWitUwks+Q/ho9uw12hmdaQrMrKO4U1/EzPvNK6+D+Bo0NHqSGVCy3qVaVK7IlOX7aNrq2q4NDu2SjXwpD6Gd9pf8KW/gWfoWBTNY3VUIa5ZodobXn75ZXw+H1OnTiUzM5OpU6fi8/l4+eWXizufKOdMfy6+9NcJbsxfe9s9+PEyUYgIhsK8MymTU1k+fntjEtXjZFirEKWRYtfyd76b90HPmIF/4YeYRtjqWMUmuHMpZu5pnO2Gl+miixBWcjTuhuKORV8/zeooVxQ6toO8b/8IuhfP4CelEFGEFEXhxl4NyM7TmbPm0IXLbQkNcPf7LcaZw/hmjccM6RamFOL6FKoYsXjxYl599VXq1auHpmnUq1ePP/3pTyxevLi484lyLHz6IHnfvET46A5cPe/B1fX/ysS5h4Zp8uH0rew8lMXoIc1pXFta7IQozRRVxdn1DrTk4YR2LME3+23MUMDqWEXONM53RVSpj60cDq0UIlIUu4aj1QDChzcTPrnX6jgFCu5agW/aqyiuCniGP4etWiOrI5U5DWvG0qZhPDNXHiDXF7xwub12K1y9f0346Hb8894r00VwUbYVqhjhdDo5c+bMRZedPXsWTZO2clE8gntW4Z38RwgH8Qx7CkeT7lZHKjKTFuxm1dYT3NS7AR2bVbU6jhCiCCiKgjN5OM5udxI+kJm/2oY/1+pYRSq4YylmzimcyWnSFSFEMdOa9wbNUyK7I0zTJLB+Kv5572FLqE+UDFMsViN71McfCJG+Yv9FlzsadsbZ5ReE9q0jsOTfFLBAohAlWqEOM48aNYq7776bX/7yl9SoUYMjR44wceJEbr755uLOJ8oZ0zDQ1+QvCaVWbYi730NlajjPvHWHSF95gN7tajKwo6wYI0RZozXvg+KqgH/e+3invoI79XHU6MpWx7puP3RF1MNWSpYyFaI0UzQ3Wou+6OunEj57BFulGlZHAvJfCwKL/01w+2LsDTvj6nkPis1hdawyrVZCNJ1bVGXu2kOktK9NpQrOC9dpLfth+rLR109Fccfi7HCjhUmFuHqFKkbcf//9JCQkMG3aNE6cOEFCQgKjR49m1KhRxZ1PlCNmIA/f/AmED2TgaNoDZ9c7ytQb3Iadp/h0zg7aNIzn9pRGcmRRiDLKUb8Diisa36zxeCe/jHvQ4yXmg8S1Cu1YhplzKv90OXntEiIiHK36o2+chZ4xHXevX1sdJ38/be7fCB/egtZuGFryCHk9iJC07vVZtfUEU5fu5c6BTS+6Tms/8oeChKsCWqv+FqUU4uoVqhihKAqjRo2S4oMoNuGzR/LPs84+ibPbnTia9S5Tb3B7j2bz3pRN1K1agXuHtcBWREvjCiFKJnuNZvlLf6a/jnfKODypj2FLaGB1rGtiGiECF7oiWlsdR4hyQ3VVwNG0J8HN8zCSR6BWiLcsi5FzCt/MNzDOHcfV854ydfpsaZBQ0U3PNjVYsP4IAzrWoWrlH1bQUBQFZ7e7MP25BJb/F8UVjaNRFwvTClF4hf5ENGnSJO68804GDBjAnXfeyaRJk4ozlyhHQvvX4/32DxDIwz3k9/ltzmWoEHHynI/xX2YQ49F4+KbWODWb1ZGEEBFgi6+LJ+1ZFM2Dd9pfCB3ItDrSNQntXI6ZcxJnO5kVIUSkaUkDQQE9M92yDOGTe/F++weMvLO4B42RQoRFhnZJxG5X+Gbxnp9dp6gqrj73YqveFP+CDwkdLJ3vN6L8KVQx4h//+AcTJkxg8ODBPPvsswwePJgPPviAf/zjH8WdT5RhpmkQWDcZ36zxqLHV8Ix8EXv1JlbHKlK5viBvfpFB2DB55KbWxEbJ0FchyhM1JgFP2rOosdXxzRpPcOcyqyNdFdMIEVg3BTU+EVsd6YoQItLU6DgcjboQ3LYIw5sV8ccP7luHd8qfwObAk/Ys9prNI55B5IuNdtKvfW1WbT3B/mM5P7tesWu4B/wOtXJNfHPeJXxitwUphbg6hSpGfPnll3z00UfccsstdO/enVtuuYUPPviAL774orjziTLK1H345/wNfc032BvegGfY06jRcVbHKlLBUJh3JmVyKsvHQyNbUSM+yupIQggLqJ5YPEPHYqveGP/8CeiZM62OVGgXuiJkBQ0hLKO1HgzhEMFNcyL6uPrG2fhnv4NauSae4c9jq1Qzoo8vfi61Ux2iXHa+XvTz7ggARfPgTh2D4qmIN/0NwmePRDihEFenUMUIn89H5coXTwOvWLEifr+/WEKJss3IPoF38suE9q/D2flWXL1/g2IvWx0Dhmny4fSt7DyUxT2Dm9OkTiWrIwkhLKRobtwDH8Verz2BFf/Dv+LzEr8Mm2mE82dFxNfFVqeN1XGEKLfUitWw12+Pvvk7TN1b7I9nGgb+pZ8QWP5f7Int8Awdi+qJLfbHFVfmcTkY1LkuG/ecZvuBs5e8jeqJxTPocRTVjm/Gaxi5pyOcUojCK1Qxonv37jz++OPs2bMHv9/P7t27GTt2LN26dSvufKKMCR3aRN43L2F4z+FOfRwtaWCZPNo2acFuVm09wU29GtCpeVWr4wghSgDFruHq+wCO5n0IZqbjX/gBphGyOlaBQruWY2afwNlueJl8nRaiNNHaDIGgD33zvGJ9HDPoxzd7PMHNc3G0GoAr5UEUu/PKdxQR0ye5FrHRGpMW7imwqK3GJOAeNAZT9+Gb8RqmPzfCKYUonEIVI55//nmioqIYNmwYbdu2JS0tDbfbzXPPPVfc+UQZYZomekY6vvTXUaMqETXiBey1Wlgdq1jMX3eI9JUH6N22JgM71bE6jhCiBFFUFWfXO9CShxPasRTf7HcwQwGrY/2MaYTzZ0XE1cVWV7oihLCaLb4uttqtCG6cVWyvGUbeWbxT/0T4YCbOrnfguuE2FFn9q8RxOmykda3HrsNZZOwuuOvBFlcH98BHMHJO4p35Bmaw5L3XCFGoV5jo6GheffVVMjMzWbJkCZmZmbz66qvExMQUdz5RBpihAP757xNY+Tn2xOT8YW4xCVbHKhYbdp3ikzk7aN0gjtv7NZKjiUKIn1EUBWfycJzd7iR8IBPv9L+WuKNWoV0rMLNPoMmsCCFKDK3NEEx/DsFti4t82+EzB/F++0eMc8dwD3gYrUXfIn8MUXS6JVUnoZKbrxfuxrjMKX/26k1w9b0f4+RefHPewQyX3G48UT5dVblTPV8dnTt3Lrt3y4RWcWVGzim8k18htGslWocb89v9HC6rYxWLvUezeW/yJupUrcB9aS2xydEEIcRlaM374Ep5AOPkPrxTX8HIPWN1JODHXRF1sNdta3UcIcR5tmqNsVVthJ6ZXqSneIUObcI7eRyYBp5hT2OXGTElnt2mMqJ7fQ6dzGPlluOXva0jMRln918SPrQp//RA04hQSiGu7LKflo4fP85DDz3EwIEDeeqpp9i5cyeDBg3ihRdeIC0tjenTp0cqpyiFQke24f3mJYzsE7gHPoyz7dAye4Tt5Dkf47/MIMaj8cioJJyazepIQohSwFG/A+5BYzByz+Cd/HKJmHye3xVxXLoihChhFEVBazsYM/c0oV0rimSb+tYF+NLfQK1QJX/FjPi6RbJdUfw6NEugTkI03yzaQyh8+QKD1rQnWsdRhHatILD8sxI/QFmUH5ctRrzwwgvExMTw1FNPYZom99xzDy+//DLLly/nrbfe4r333otUTlGKmKaJvnkuvul/RXFGETXi+TJdZc/1BXnrywzChskjN7UmNloGPQkhCs9eoxmeoU+BEcI7ZRzh47ssy5K/gsb3XRHtLMshhLg0W+3WqJVro2+YcV1HuE3TILDqSwKLJ2Kr1eL8EuuVr3xHUWKoisLInvU5leVnUcaVC9la68E4WvYnuGkO+oZpEUgoxJVdthixfv16XnzxRXr27MkLL7zAmTNnSElJASAlJYUjR6w/giNKFjMcJLDoIwJLP8FWuyWeEc+jVqxudaxiEwwZvPv1Rk6e8/HQyFbUiI+yOpIQohSyxdfFk/YsijMK7/RXCR3ItCRHaPdKzKzjaO2kK0KIkkhRFLQ2gzHOHSG0b/01bcMM6fi/ew99w3QczXrhHvAIiuYu4qQiElrVj6NxrVimLt1HQA9f9raKouC84VbsDW9AXz0JfdvCCKUUomCXLUYEg0E0TQPA7Xbj8Xgu2jmRFh/xY99PYQ5uX4zWdijuAQ+jaB6rYxUbwzT5cPoWdhw8xz2Dm9OkTiWrIwkhSjE1JgHPsGdQY6vjmzWe4I6lEX38H2ZF1MaeKLMihCip7PU7oMQkoG+YdtX74oYvO7/guWcVzk434+x2F4oqp5aWVoqicGOvBmTl6cxde7AQt1dx9boHW+0kAosnEty7NgIphSiY/XJXhsNhVqxYceGFLhQKXfSzYcgAFJEvfHwXvjnvYuo+XCkP4qjfwepIxW7Swt2s2nqCUb0a0Kl5VavjCCHKANUTi2foWHyz38a/4J+Y/my0pNSIPHZ+V8QxnP0eQlFkAK8QJZWi2tBaDyKweCLhw1sKvVS6ce4o3plvYuadLTf7auVBo1oVad0gjvQVB+jVtiZRLsdlb6+odtwpD+Kd/ir+ef9ASR2DvUazCKUV4mKXLUbExcXx9NNPX/i5YsWKF/1cubKcWyZA37aQwJKPUaIq4Rk+Blvl2lZHKnbz1x268KKf2qmO1XGEEGWIorlxpz6Gf977BFZ8juHNxtnp5mI9bcI0jPyuiMq1sSfKrAghSjpH467oa79F3zCtUMWI0NHt+Ga/jaKoeIY8ia1qwwikFJEysmcDXvxoFTNW7OemXlf+f6s4nHgGPop36iv4Zr2NZ+hYGV4qLHHZYsS8efMilUOUQqYRIrDsvwS3zMNWswXuvvejuKKtjlXsNuw6xSdzdpDUII5f9Gsk51ULIYqcYnPg6vsAgWWfEMxMx/Rn4+rxKxT1sm/b1yy0e0V+V0TKg9IVIUQpoNgcaEkDCaz4H+Hjuy5bXAjuXIZ/4UeoFeJxpz6GGpMQwaQiEmonRNOpRVW+W3OIlOTaVKpw5WHqiisad+rjeCe/jC/9dTxpz8rvhog42eMQ18TwZeOb/leCW+bhSBqIO/WxclGI2Hs0m/cmb6JO1Qrcl9YCmyp/QkKI4qGoKs6ud6AljyC0Yym+2e9ghgJF/jimYaCvm4JauRb2eslFvn0hRPFwNOsFzij0DdMveb1pmgTWTcE/fwK2qg3kw2YZN7xbPcKGydRl+wp9HzW6Mu7Bj4Nh4J3+VwzvueILKMQlyCcpcdXCJ/fh/fpFwif24Or9G1ydby0Xw49OnfMx/qtMKrg1HhmVhEsrniOUQgjxPUVRcCan4ex2F+GDmXin/xXTn1ukjxHasxIj69j5FTRkt0CI0kJxuNBa9iO0fz3hM4cuus4Mh/Av/BB9zdfYG96Ae9Dj5eKgUXmWUMlDj9Y1WJxxhBNnvYW+n61iDdypj2H6svGlv46pF/6+Qlwv2esQVyW4cxneKeMA8KQ9g6NRF4sTRUaeP8ibX2YQChk8enNrYqOv3P4mhBBFRWveG1fKgxgn9+Gd8gpG7uki2e6FrohK0hUhRGmktUgBu/Oi7ggzkIcv/XVCO5agtUvD1fs3KLbLDzUUZcPQronYVIVvF++9qvvZEurj7v9bjLNH8M0ajxnSiymhEBeTYoQoFNMI41/xv/xWv4T6eEa+iC0+0epYEREMGbwzaSMnz/n47Y2tqBEfZXUkIUQ55KjXHvegMfnLKE8eR/jskeveZmjPKoxzR9GSh0lXhBClkOKKxtG8N6HdKwmeO46RczL/9eHYDly9fo2z/QiZbVWOVIx2ktK+Niu2HOfA8Zyruq+9VktcvX5N+Oh2/PPewzTCxZRSiB/Inoe4ItOfiy/9DYKZM3E074t78BOo7hirY0WEYZp8OH0LOw6e4+7BzWhSp5LVkYQQ5Zi9RjM8Q8eCEcI7ZRzh47uueVs/dEXUxF6vfRGmFEJEktZqACgqp9L/iffbP2J4z+Ee9DiOxl2tjiYskNq5Dh6nna8X7bnq+zoadsbZ5ReE9q0jsOTfmKZZDAmF+IEUI8Rlhc8cJO+blwgf3Y6zx69wdbuj2Ka5l0RfL9zDqq0nGNWrAZ2bV7M6jhBCYIuviyftWRRnFN5prxI6kHFN28nvijgisyKEKOXUqEo4GnfFt2c92J140p7FXqOZ1bGERaJcDlI71yFz92l2HLz6gZRay35obYcS3LYIffWkYkgoxA9k70MUKLhnNd5vX4ZwEM/QsWhNe1odKaLmrz/MjBX76dW2Jqmd6lgdRwghLlBjEvAMewa1YnV8s8YT3LH0qu5vGgb6+imolWpgry9dEUKUdlr7EcTeMBxP2rPYKtWwOo6wWEr72sRGa3y1cPc1dTdo7UfiaNoLfcM09I2ziiGhEPmkGCF+xjQNAqsn4Z/7N9TKNfGMeOGy61eXRRt2neKT2dtJahDHL/o1kvMthRAljuqJxTN0LLbqTfAv+Cd6Znqh7xvauxrjrHRFCFFWqJ6KxPW5A9UTa3UUUQI4HTaGdUlk16EsMndf/cBjRVFwdrsTe2IygeWfEdy5rBhSCiHFCPETpu7FN2s8+vqpOJp0xzP0KdSo8jUnYe/RbN6bvIk6CRW4L60FNlX+TIQQJZOiuXGnPoa9fgcCKz7Hv+J/mKZx2fuYpoG+bnJ+V0S9DhFKKoQQIpK6t65BQkU3Xy/ag3EN3RGKquLqcy+26k3xL/iQ0MHMYkgpyjv5lCUuMM4dxfvNHwgf3ISz6//h7HF3uVsK6tQ5H+O/yqSCW+ORm5JwaeVnPoYQonRSbA5cfe7H0bwPwcyZ+Bd8iGmECrx9aM+a/K6ItsNQpNgqhBBlkt2mMrx7PQ6eyGXV1uPXtA3FruEe8DBq5Vr45rx7XUOThbgU2QsRAIQObCDvmz9gBvJwD34CrUVKuTs1Ic8f5M0vMwiFDB65uTWx0U6rIwkhRKEoqoqz6x1o7UcQ2rkU36y3MYOBn93uQldExRrY63e0IKkQQohI6di8KrWqRPPtor2EwpfvmivI9x14iqci3plvEj57uIhTivJMihHlnGmaBNZNwTdzfP5AtJEvYq/R1OpYERcMGbw7aSMnz/n47Y2tqBkfZXUkIYS4Koqi4GyXhrPbXYQPbcQ7/VVMf+5FtwntXYNx9jBaO+mKEEKIsk5VFG7sWZ8T53wszjx67dvxxOIZ9DiKasc343WM3KufQyHEpcieSDlmBv345/4Nfc3X2Bt0wpP2NGp0nNWxIs4wTT6asZXtB89x96BmNKlTvmZkCCHKFq15b1wpD2Kc2o93yisXdhpN00BfOwW1YnXpihBCiHIiqUEcDWvFMmXpXgLB8DVvR41JwD1oDKbuwzfjtZ8Vu4W4FlKMKKeM7BN4J79MaN9anJ1vwdXnXhR7+Twt4ZtFe1i55Tg39qxP5xbVrI4jhBDXzVGvPe5BYzDyzuKdPI7w2SPkbVuJcfZQ/goa0hUhhBDlgqIojOrZgKxcne/WHrqubdni6uAe+AhGzkm8M9/ADPqLKKUoryyfznfo0CEefPDBCz/n5OSQm5vLqlWrLExVtoUObebNN18AACAASURBVMb33d8BcKeOwV6rpcWJrLNg/WGmL99PrzY1GNS5rtVxhBCiyNhrNMMzdCy+9NfxThmH7qkgXRFCCFEONa5dkaQGccxYvp+ebWoQ5br2AfX26k1w9X0A/5x38M15F/eAR1Bsln+kFKWU5YdGatWqxeTJky/817dvX4YMGWJ1rDLJNE30zJn40l9D9VQkasQL5boQkbn7FB/P3k5Sgzh+0b9xuRvYKYQo+2zxdfGkPYvijCJ09pjMihBCiHJqZI/6eAMhZq48cN3bciS2w9X9V4QPbcK/4IMrLiktREFKVBlL13WmTp3Khx9+aHWUMscM6fgX/YvQruXYE5Nx9RqNormtjmWZfcey+ce3m6mTUIH70lpgk51zIUQZpcYk4El7Fk/WLnwJbayOI4QQwgJ1qlagU/OqzFlzkL7Jtah4navGOZr2wPDnoK/6koC7As4bbpcDe+KqlahPYPPmzaNq1aq0aNHC6ihlipF7Gu+UVwjtWo7WfiSufg+W60LEqXM+/r+9O4+Lqtz/AP6ZYdgXQTbZREBBcAFFwXJBMRVNQEBDc2m7drXrVrZo3jZvWmk/uy6Z3W5laVYuuJJZ7uYG7hu4oCKgsoggO7M8vz+QuZJKLsOcGfi8X69eOTPMme98OZxz5jPPec78VSdgY2mKKcM6wsLMoDI5IiKdk1vawbZDBEdFEBE1YUN6+kCtFti477JOlmcWPAimHQZAeep3VB/bpJNlUtMiE0IIqYuoNXbsWPTs2RNjxoyRupRGo+LKGeSumQuhUsIldjKs/btKXZKkSsur8eaiPSgsrsSciT3RsoWd1CUREREREenF4tXH8dvBTCyZ1hctHB//UvZCaJC/YSFKT+2G06BxsOvUTwdVNl0aVTU0FaXQVJRAXVEKTUUp1JUl0FSUQqYwg13oAMjkJlKXqTMG85Vwbm4uUlNTMWfOnId+7o0bpdBoDCZT+UvOzrbIzy9p0NcQQkCZtgNVe3+AzM4ZloMnodzeHeUN/Lr69jC9VKo0mPfzMVzNL8PUxBBYmsga/PdgTPSxXjYV7KXusJe6w17qDnupO+yl7rCXutOYe/lUZw9sS72Cr9efxMvROhqN3m0MTIqLULD5S5QqFTD16aJ9qDH3sj5CVQ1RVQZRVQpRWXr732UQlWVAVent+8v+d//t21BX33eZJtb2qHLrDJn544dI+iKXy+DoaHPfxw0mjFi7di0iIiLg4OAgdSlGT6iVqNq7HMr0XTDx6gjLyL8b1UrbEDRC4Jtf0nA2qwgvRwehrTfXMyIiIiJqWhxszdG3iyd+PXAFA8O94eVy/w+KD0omV8DyqX+g/Je5qNy2BLJBU6FwD9RBtdISQgDq6jtCg7rBAqrK7rh9Z+BQCqiV91+wXAGZhQ1k5taQmVtDbusEmXMrwNwaMvPb91vc+e+a/zu7OaGgoFRv718fDCqMmDFjhtRlGD1NeREqfl8ETe4FmIUMhlmXeJ4jDGDt7os4eCYXCRG+6NauhdTlEBERERFJYlA3b+w8ehVJuzIweViwTpYpMzWH1YApKN84GxVb5sMqejpMnLx1suzHJYQAVNV3BQZ1RiRU1R29IG6PXoBadf8FmyhuBwY2kFlYQ27nApm5TU2ocI8wQXY7bIDC7JEm+2yME4QaTBixZcsWqUsweuq8DFT8thCiuhwWT70CU15LHgCw81gOkm9fV3lQN8PYKBIRERERScHawhSDurXEml0XcT67CG087XWyXJmFDSwHvo7y9R+iYvP/wSpmBuBsq5NlA7WhQtU9w4Taf9cdrXDH/fWGCqZ1Ryo0c4XM3Bcyi9vBQu1/FjZ1Ri7A5NFCBfofgwkj6PEoz+5B5Z7vILN2gFXsOzBx9JK6JINwIqMAy7ecQ0c/R4zq788NBhERERE1eU+FeuH3Q9lYszMDb43srLNjZLlNc1g+/Toq1s9G+S+fQvXCR/jzR04hBKCsvCswuPfcCnUDB2jqCxXM/hQqtNCOUMDt0Qv3DBYUZjp57/TwGEYYOaFRoWr/T1Ce3goTjyBY9n2lJsUjZF4vwRfrTsPLxQbjYtvBhKerEBERERHB3MwE0U+2wg+/n8PJi4Xo6Oeos2Wb2LvDcuBrKN/0Ca4tfwfCtsVdcytAo77/AhRm2lMfZOY2kNu71zndoe7cCnecAsFQwegwjDBimopbqNy6GOpr6TDtMADm4c80qku9PI6C4gr8e9Vx2FgqMHlYR1iYcVUnIiIiIqoVEeKOLSlXkLQrA+19m0OuwxHEJi6+sOw/CarUn6EpvVEzUsHB/XbI8L8AAdq5FW6HD2ZWDBWaEH5CM1LqgkxU/LYAoqIYFr3HwtS/u9QlGYyySiU+W3kc1SoNXh8RCnsbc6lLIiIiIiIyKAoTOeJ6+uKrTWeQmpaH8CBX3S7fsx3cOn3WJC/tSQ+G49aNkPLCAZSvnwUIAauYGQwi7qBUafB50knk3azAxPgO8HBq2pc0JSIiIiK6n/AgV3g6W2PtnotQqTVSl0NNDMMIIyI0GlQdXInK7Utg4twKVnHvwcTZR+qyDIYQAt/+kob0K0V46elAtPV2kLokIiIiIiKDJZfLEN/LD3k3K/DHiWtSl0NNDE/TMBKiqgwV276AOvsUTIMiYf7Es5CZ8Nd3p6TdF3HgTC7ie/miW7sWUpdDRERERGTwgls7orVHM2zYewlPtm8BM1POQUf6wZERRkBdmIOytR9AfTUN5j2fh0WPMQwi/mTnsRwk789Er2B3PP2Et9TlEBEREREZBZlMhoQIXxSVVmPbkWypy6EmhGGEgVNePozy9f8ClFWwGjwNZoG9pS7J4JzIKMDyLefQ3rc5Rg/w19l1komIiIiImoKAlg5o79scv+zPRHmlUupyqIlgGGGghNCg6tBaVP62EHJ7d1jFvw+TFm2kLsvgXMguwhfrTsPTxRrjY9vDRM5VmoiIiIjoYSX08kNZpQq/plyRuhRqIjjW3wCJ6gpU7vgPVJlHofDvUXNaBq+3e5f8ogp8/MMR2FgqMHloMCzNuToTERERET0K7xa2CAt0wW+pWejb2RPNbMylLokaOX6NbGA0RddRvu5fUF05DvMnR8Ii4iUGEfeQnV+K2csPQ6nSYMqwYDjYcmNJRERERPQ44nr6QqUS2LQvU+pSqAngV8kGRHXlOCq2L4FMZgLLp9+Awj1Q6pIM0oXsYvx71XGYmcrx8T96wErBOSKIiIiIiB6Xa3Mr9Ax2w85jOegf5gVne0upS6JGjCMjDIAQAlXHNqHi139DbusMq/j3GETcx4mMAnz601HYWJni7VGh8Hazk7okIiIiIqJGI6a7D+RyGdbtuSR1KdTIMYyQmFBWoXLbF6hOWQ2FXxisYmdAbussdVkGaf/p61i45iRaOFrh7VGhcGJSS0RERESkUw625ugb6okDp68jO79U6nKoEWMYISHNrXyUr/8QqoupMAt7BhaR4yBTcO6De/n9UBa+2ngGrT2a4a1nO8POmvNoEBERERE1hEHdvGFhboKkXRelLoUaMc4ZIRFVzhlUbl0MITSwHPgqFF4dpS7JIAkhsG7PJWzcdxmd2jhhXGw7mCpMpC6LiIiIiKjRsrE0RVS4N9buvogLOcVo7dFM6pKoEeLICD0TQqA4ZRMqfvkUMis7WMe9yyDiPjQagWW/ncPGfZfRs6MbXolrzyCCiIiIiEgP+nXxhJ2VKdbszIAQQupyqBFiGKFn6mvpuPH7t1B4h8Aq9h3Im7WQuiSDpFRpsGTDaew8moOB3Vri+YFtYSLn6kpEREREpA8WZgpEd/fB2awinL5UKHU51Ajx052embi2RosR78Ki3wTIzDgB471UVqswf/VxHErPwzN9WmNY79aQyXj5TiIiIiIifYoIcYdTMwus3pUBDUdHkI4xjNAzmYkprHyDIZOx9fdSUl6NuT8eRXpmEV4cFIio8JZSl0RERERE1CQpTOQY0tMHV3JLcSg9T+pyqJHhJ2IyGDeKK/HxD0eQlVeGf8S3R4+OblKXRERERETUpHULagEPJ2us3X0RKrVG6nKoEWEYQQbhakEZZi8/jKLSKkxNDEanNs5Sl0RERERE1OTJ5TLER/gi92YF9p68JnU51IgwjCDJXbx6Cx//cARqtQZvPdsZAS0dpC6JiIiIiIhuC2ntBD8PO2zYexnVSrXU5VAjwTCCJHX6ciHm/ngUFmYmmD46FC1dbaUuiYiIiIiI7iCTyZDQyw83S6qw/UiO1OVQI8EwgiSTmp6Hf688Dmd7C7w9OhSuDlZSl0RERERERPfQ1tsB7X2aI3n/ZZRXqqQuhxoBhhEkiR1Hc7Bk3Sn4uNvhrZGdYW9jLnVJRERERERUj4QIP5RVqvBryhWpS6FGgGEE6ZUQAhv3XsKyLWfRwc8RUxNDYG1hKnVZRERERET0F7xb2KJrWxf8npqF4rJqqcshI8cwgvRGIwR+3Hoea/dcwhPtWmBCfAeYm5pIXRYRERERET2guF6+UKo0SN53WepSyMgxjCC9UKk1+O+mM9h6OBv9unjhpcGBUJhw9SMiIiIiMiYtmluhR0c37Diag4KiCqnLISPGT4PU4KqUaixccxIHTucivpcvhvdtDblMJnVZRERERET0CGK6t4JMJsP6Py5JXQoZMYYR1KBKK5T4v5+O4dSlGxgTFYDBT9ZsuIiIiIiIyDg1t7NA31AP7Dt1HTn5pVKXQ0aKYQQ1mJslVfhkxRFcvn4L42Pbo3eIh9QlERERERGRDjz9RCtYmJsgafdFqUshI8UwghpEbmE5Plp+GAXFlZgyLBhd2rpIXRIREREREemIjaUpBoS1xNHzBcjIKZa6HDJCBhFGVFVV4b333kP//v0RHR2Nd955R+qS6DFkXi/BR8sPo7JajTdHdEJQq+ZSl0RERERERDrWv6sXbK1MsWZXBoQQUpdDRkYhdQEAMHfuXJibm2PLli2QyWQoKCiQuiR6ROmZN7FgzQlYWSgwNTEEbo7WUpdEREREREQNwMJMgcFPtsKPW8/jzOWbaOfDLyHpwUk+MqKsrAzr1q3D5MmTtRMbOjk5SVwVPYoj5/Ixb+VxONia4+1RoQwiiIiIiIgaud4hHnC0s8Bqjo6ghyR5GJGVlQV7e3ssWrQI8fHxGD16NA4dOiR1WfSQ9hy/is/XnkRLVxtMHxWK5nYWUpdEREREREQNzFQhx5CePsi8XoLDZ/OlLoeMiExIHF+dPn0a8fHx+PTTTxEdHY3jx49j3Lhx+P3332FjYyNlafSA1mw/j6XJZ9DJ3xnTnw+DpblBnP1DRERERER6oNYITPx0BzQagc/f6AMTE8m/8yYjIPmnRjc3NygUCgwePBgAEBwcDAcHB1y6dAkdOnR4oGXcuFEKjcZ4hgQ5O9siP79E6jIemxACq3Zk4NeUKwgLdMHfBgeh9FYF9Hml4cbSS0PAXuoOe6k77KXusJe6w17qDnupO+yl7rCXjya2eyssSjqJdTvOo1ewOwD2UpeMsZdyuQyOjvcfYCB5ZNW8eXOEh4dj7969AIBLly7hxo0b8Pb2lrgyqo9ao8G3v6Tj15Qr6NPZAy9Ht4OCCSgRERERUZPUqY0TfN3tsP6PS1Cq1FKXQ0bAID49fvDBB/jyyy8RHR2N1157DXPmzIGdnZ3UZdF9VCvVWLz2FP44eQ0x3VthVD9/yOUyqcsiIiIiIiKJyGQyJET44WZJFbYfyZG6HDICkp+mAQBeXl5YtmyZ1GXQAyivVGHBmhM4l1WEkf380TfUU+qSiIiIiIjIAAR6O6BdKwck78/UnqpBdD8GMTKCjENxWTXmrDiCjJxivBwTxCCCiIiIiIjqiI/wQ2mFEltSrkhdChk4hhH0QPKLKvDR8sO4frMck4Z2RLegFlKXREREREREBsbHzQ5dApyxJTULRSVVUpdDBoxhBP2l7LxSzF5+GGUVSrw+vBM6+DpKXRIRERERERmouF6+qFaqsWrbOalLIQNmEHNGkOE6n12E+atOwMxUjmkjO8PD+f6XZiEiIiIiInJztEaPDm74Zd9llFdUIyzQFX7udpDJOOk9/Q/DCLqv4xcK8MW6U3CwNcfUxBA42VtKXRIRERERERmBhAg/qAHsPHoVWw9lw9HOAmGBLggLdEVLVxsGE8Qwgu5t/6nr+Do5DV4uNnj1mWDYWZtJXRIRERERERkJO2szTH8uDJlZN3H0fD5S0vLwW2oWNh+8AlcHS4QFuiIsyBUeTtZSl0oSYRhBd/k9NQs/bjuPti3tMTGhIyzNuZoQEREREdHDs7JQoHsHN3Tv4IbSCiUOn81DSloeNu2/jI37LsPD2bommAh0gauDldTlkh7xUyZpCSGwds9FbNqXiVB/Z7wcEwRThYnUZRERERERUSNgY2mKiBAPRIR4oLi0CofO5uNgWi7W7r6ItbsvwruFLcIDXdG1rQscm1lIXS41MIYRBADQaASW/3YWO49dRa9gN4wZ0BZyOc/jIiIiIiIi3WtmY46+oZ7oG+qJwluVSEnLQ0paLlbuuICVOy6gtWczhLV1Qde2LmhmYy51udQAGEYQlCoNvtp4GofO5mNQN28kRPhyQhkiIiIiItKL5nYWiApviajwlsi9WY7U28HEiq3nb58+7oCugS7oEuACG0tTqcslHWEY0cRVVKmwKOkk0jJv4pk+rREV3lLqkoiIiIiIqIlydbDC4CdbYfCTrZBTUIbUtFwcTMvD97+exQ+/nUNQq+YIC3RBpzbOsLLgx1ljxt9eE1ZSXo3PVh7HldxSvPR0ILp3cJO6JCIiIiIiIgCAh5M1PHr6IraHD67kliIlPRcpZ/LwdXIaFCbp6ODriPAgVwT7OcHcjHPdGRuGEU3UjeJK/N/Px3DjViUmxHdASBsnqUsiIiIiIiK6i0wmg3cLW3i3sMXQCD9cvHqrZo6J9FwcPV8AM1M5Qlo7ISzQFR18m3MSfiPBMKIJulpQhv/7+Rgqq1WYmhgCfy97qUsiIiIiIiL6SzKZDH4ezeDn0QyJka1xPrsIKWl5SE2vuWSopbkJOrVxRligK4JaOUBhIpe6ZLoPhhFNzMWrt/DvVcchl8vw1rOd0dLVVuqSiIiIiIiIHppcLkNASwcEtHTAs/3aIC3zJlLO5OHwuXzsO3Ud1hYKhAa4IDzQBQEtHXi1QAPDMKIJOX2pEIuSTsLO2hRTE0Pg4mAldUlERERERESPzUQuR3sfR7T3ccToAQE4fakQKWm5OHgmF7uPX4WdtRm6BrggLMgFfh7NIOfVAyXHMKKJSEnLxVcbz8DN0RqvJQbDntfqJSIiIiKiRshUIUdIGyeEtHFClVKNkxk3cDAtF7tPXMW2I9lobmeOrm1dEBboilYtbCFjMCEJhhFNwI4j2Vj+2zm09myGyUM7wsqC1+YlIiIiIqLGz9zUBF3auqBLWxdUVKlw7EIBUs7kYuuhbGxJyYKLvSW6BrogPNAVHs7WDCb0iGFEIyaEwMa9l7Huj0sI9nPEuCHtYW7KmWWJiIiIiKjpsTRX4Il2LfBEuxYoq1TiyNl8pKTlYvOBK0jenwl3J2uEBdaMmGjRnKe0NzSGEY2URgj8uPU8th3OxpPtW+D5gW05kywREREREREAawtT9Ax2R89gd9wqq8bhs3k4mJaH9XsuYd2eS2jpaoPwQFd0besCJ3tLqcttlBhGNEIqtQbfJKfhwJlc9O/qhWciW3OCFiIiIiIionuwszZDn86e6NPZEzdLqm5fJjQXq3ZmYNXODPi52yEs0BVd2rrAwZZz7+kKw4hGpqpajc/XncSpi4VIiPDFoG7ePO+JiIiIiIjoATjYmqN/Vy/07+qF/KKKmmDiTC5+3HYeP207D38ve4QFuSI0wBl2VmZSl2vUGEY0IqUVSsxffRwXr97Cc1EBiAjxkLokIiIiIiIio+Rsb4lB3bwxqJs3rt0oQ2paHg6m5WLZlrP44bdzCGzlgLBAF4T6O/MiAY+AYUQjcbOkCvN+Pobcm+V4ZUh7hAa4SF0SERERERFRo+DmaI2YHj6I7t4K2fllSEnLRUpaLr79JR3f/3oWHXwdERbogpA2TrAw48fsB8EuNQK5heX49KdjKK1U4tVhwQhs1VzqkoiIiIiIiBodmUwGLxcbeLnYIL6XLy5fL7kdTOTh2IUCmCnk6OjniLBAV3T0c4QZr2Z4XwwjjFzm9RLMW3kMQgBvjugEHzc7qUsiIiIiIiJq9GQyGXzc7ODjZodhfVrjQnYxUtJycSg9D4fO5sPczASd2ziha6Ar2vs059UN/4RhhBFLy7yJhWtOwNpCganDO/FauERERERERBKQy2Tw97KHv5c9RjzVBmevFCElLReHz+Zj/+lcWFso0NnfGWGBrmjrbQ8TOYMJhhFG6vDZfHy54RRcHKzw2jPBaG5nIXVJRERERERETZ6JXI6gVs0R1Ko5RvUPwJnLhTh4Jg+p6XnYc+IabK1M0aWtC8LauqCNlz3kTfTqhwwjjNDu41fx3a/p8HWzw+RhwbCx5MytREREREREhkZhIkdHPyd09HOCUqXGiYxCpKTlYu+Ja9hxJAcOtubo2tYFYYGu8HGzhawJBRMMI4zM5gOZWLUzA+19muMfcR1gbsYJUYiIiIiIiAydqcIEoQHOCA1wRmW1Cscv3EBKWi62H8nGb6lZcGpmgbBAV4QFusDLxabRBxMMI4yEEAKrdmTg15QrCAt0wd8GB3ECFCIiIiIiIiNkYaZAeJArwoNcUV6pxNHzBTiYlotfD17BLwcy0aK5FcICa0ZMuDtZS11ug2AYYQTUGg2W/pKOvaeuI7KzB57t599kzysiIiIiIiJqTKwsTNG9gxu6d3BDSXk1Dp/LR8qZXGzcexkb9l6Gp7MNBj7ZCt3aOjeq0RIMIwxctVKNJetP49iFAsT28EFM91aNagUkIiIiIiKiGrZWZugd4oHeIR4oKq1CanoeUtPysGJLOjr6OMDaovHMF8gwwoCVV6qwYM0JnM8qwsh+/ugb6il1SURERERERKQH9jbm6NfFC/26eMHJyQYFBaVSl6RTDCMMVHFpFeatPI6rBWV4OaYdwoNcpS6JiIiIiIiIJNAYR8cbRBgRGRkJMzMzmJubAwBef/119OzZU+KqpJNXVIF5Px1DUVkVJg/tiPa+jlKXRERERERERKQzBhFGAMCCBQvg7+8vdRmSy8orxbyfj0Gl1uCN4Z3g59FM6pKIiIiIiIiIdMpgwggCzmUVYf7qE7AwM8G0EaHwaKSXcCEiIiIiIqKmzWDCiNdffx1CCISGhuK1116DnZ2d1CXp1fELBVi87hSa21lgamIwnJpZSl0SERERERERUYOQCSGE1EVcu3YNbm5uqK6uxqxZs1BWVoZPP/1U6rL0ZvuhLMz/+Sh83e3w/tgn0MzGXOqSiIiIiIiIiBqMQYQRdzp79izGjx+P7du3P/BzbtwohUZjUG+jXs7OtsjPLwEA/JaahZ+2nUegtwMmxHeApbnBDFYxCnf2kh4Pe6k77KXusJe6w17qDnupO+yl7rCXusNe6g57qTvG2Eu5XAZHR5v7Pi75J9/y8nKo1WrY2tpCCIFffvkFgYGBUpfV4IQQSNp9Ecn7MxHq74yXY4JgqjCRuiwiIiIiIiKiBid5GHHjxg1MnDgRarUaGo0Gfn5+eO+996Quq0GpNQLfbzmLXceuolewO8YMCIBc3viuG0tERERERER0L5KHEV5eXli3bp3UZeiNUqXBnGWp2HfiGp5+whvxvXwhkzGIICIiIiIioqZD8jCiqbmQXYR9J65heGRr9A9rKXU5RERERERERHrHMELP2no74Lv3BkBdpZS6FCIiIiIiIiJJyKUuoKmRyWRobmchdRlEREREREREkmEYQURERERERER6xTCCiIiIiIiIiPSKYQQRERERERER6RXDCCIiIiIiIiLSK4YRRERERERERKRXDCOIiIiIiIiISK8YRhARERERERGRXjGMICIiIiIiIiK9YhhBRERERERERHrFMIKIiIiIiIiI9IphBBERERERERHplULqAnRBLpdJXcJDM8aaDRV7qTvspe6wl7rDXuoOe6k77KXusJe6w17qDnupO+yl7hhbL/+qXpkQQuipFiIiIiIiIiIinqZBRERERERERPrFMIKIiIiIiIiI9IphBBERERERERHpFcMIIiIiIiIiItIrhhFEREREREREpFcMI4iIiIiIiIhIrxhGEBEREREREZFeMYwgIiIiIiIiIr1iGEFEREREREREesUw4gFFRkbi3LlzUpdhlCIjIxEVFYXY2FjExsZi9uzZ9/3ZpKQkTJo0SY/VNS6RkZHo0aMH1Gq19r6kpCQEBARg+fLlOnmNgwcPIj4+XifLMjbFxcXo2LEjPvzww0dextixY3HlyhUAwOjRo7Fjxw5dlWdU9LGuNhXcP+neg/SUfdfNNvFxLFy4ENXV1ZK89l/ZvHkzhgwZgtjYWERFRWHq1KmPvKxbt27hq6++0mF1NbKzsxEeHq7z5UqhuroaH3/8MZ566ilERUVhyJAh2Lp1a73Pyc7Oxs8///xAy29MvQJqtl+DBw+GRqOpc5/U2zRDqOFh1X7OiYmJQb9+/TB+/HgcOXJE6rKMppcMI4zInQftxmbBggVYv3491q9fj7ffflsny9RVP1QqlU6WYyhcXFzwxx9/aG+vXbsW7dq1e6hlNLae6MqmTZsQHByM5OTkhz4A1mg0EELgq6++QsuWLRuoQuOii3WViKTzONtEXVi0aBGUSqXeX/ev5OXl4YMPPsAXX3yB9evXY/PmzXjppZceeXm3bt3Cf//7Xx1WqFuGcHz6/vvv4/r160hOTsavv/6KOXPmYObMmUhNTb3vc3Jych44jNAVQ+hVrfLycqxfv17qMnROimPYBQsWYMOGDfj9998RFxeHl19+GcePH9d7Hbqmj14yjHhI33zzDRISEjBkyBAkJiYi8jgZdAAAFfdJREFULS1N+1hAQACWLFmChIQE9O3bF1u2bAFwd5p6522VSoWXXnoJ8fHxePrppzF9+nTtDj0pKQnPP/88/vGPf2Dw4ME4ffo0Bg8eXKeemJgYg0jfHtbatWsxbNgwxMfHY8yYMbh48aL2sZKSEowbNw6DBg3CmDFjkJubC+Dufpw7d+6u1O/O25988gkSEhIQExOD5557Djk5OQD+1/9PPvkEcXFxWLVqFXr06IG8vDztcj788EMsWbJEH63Qubi4OCQlJQEAsrKyUF5eDn9/fwDA/v37kZiYiCFDhiA6OhrJycna540ePRqzZs3CM888g/HjxwMAvvzyS0RHRyMmJgbDhw/XJuhqtRrvvvuu9rGMjAw9v0tprFmzBq+88goCAgKwbds2ADXfzE2ePBljxoxBVFQUJk6ciJKSEu1jkyZNwosvvohBgwbh1q1bRpNU68OjrKsnTpxoNNtBXatvexgZGYn58+cjMTERkZGRdUafXLx4EX/729+028s1a9bovXZDVV9PazXldfJe28Rp06bVWb/uvJ2bm4vnnnsOTz/9NMaNG4dx48ZpH/vzSLE7by9atEg7wnLIkCG4desWPvjgAwDA8OHDERsbi1u3bunlPT+IgoICKBQK2NvbAwBkMhmCgoIAAMePH8fo0aMRHx+P+Ph47Ny5E8D/jk0+/vhjREdHIzo6GocOHQIAzJw5EyUlJYiNjcXw4cMB1AQekyZNwtChQxEdHV3nmCUyMhKfffYZEhMT0bt3b2zcuBFLly7F0KFD0a9fv7s+oN/rNQFg165dGD58OOLj45GYmIhjx44BqBkhGR0djenTpyM2Nha7d+9umEY+oJycHGzevBnvv/8+zM3NAQD+/v4YN24cFi1aBODexzMzZ85ERkYGYmNjtaNyT5w4gcTERERHRyMxMREnTpyo81rG3qs7TZgwAYsWLborSMzMzMRzzz2H6OhoxMXFaWtevHhxndHNN2/eRHh4OMrLy1FdXY1PPvkEQ4cORUxMDN544w2UlZUBqNkGvPvuuxgzZgz69OmD2bNnY//+/Xj22WcRGRmJ7777rs7rb9iwAfHx8ejXr98D76sCAgKwcOFCJCQkaH/nUunfvz+GDx+Or7/+ut6+lJSUYPr06dr1cubMmQDQ9Hop6IH06dNHnD17Vty4cUN73969e8WwYcO0t/39/cWyZcuEEEIcOnRI9OjRQwghRFZWlggLC9P+3J23NRqNKCws1P77jTfeECtWrBBCCLFmzRoREhIiMjMztc8dNmyYOHjwoBBCiNTUVBEbG9sQb1en+vTpIwYMGCBiYmJETEyMWLhwoRg7dqyoqqoSQgixc+dOkZiYKISoec8dOnQQGRkZQgghFi5cKCZOnKh97M/9qP293Ov2nb+rlStXiilTpgghavrv7+8vkpOTtY/PnTtXLFy4UAghRGlpqejWrZsoKCjQeS8aWp8+fUR6erqIiooSRUVFYv78+eL7778Xb731lli2bJkoKioSKpVKCCFEfn6+6NmzpygqKhJCCDFq1Cjx97//XSiVSiGEEElJSeKZZ54RJSUlQgihXU8PHDgggoKCxOnTp4UQQixevFi89tpr+n6repeWlib69OkjNBqNWL9+vXjppZeEEEIsWLBAdO/eXeTn5wshhJg2bZr4+OOPtY9FRETUWRfvXEdHjRoltm/frud3YhgeZ101xu1gQ6pdp+rbHvbp00e7XmZlZYmQkBBRWloqlEqliIuLExcuXBBCCFFSUiL69++vvd1UPWhPa//dFNfJ+20Ta/+Ga915e8KECeLzzz8XQgiRnZ0tOnXqpH3sz9vD2ts3b94UoaGhoqKiQghRs47W7qf8/f1FaWlpw7/Zh6RWq8X48eNFWFiYmDhxovj2229FYWGhKC4uFrGxsSI3N1cIIURubq7o2bOnKC4u1h6brF27VghRs6/t2bOnqKqquus4Ugghnn/+eZGSkiKEEKKqqkqMGDFC/PHHH0KIun/vx48fF8HBwWL58uVCCCGSk5PF8OHDhRCi3tfMzMyscwxw7tw5ERERof25tm3biiNHjjRUCx/K9u3bRUxMzF33nz59WoSFhdV7PBMXF6f9+aqqKhERESH27dsnhKg5zo+IiND+DhpDr2rVbr8mTpwoli5dWue+oUOHipUrVwohhDh//rwICwsTN27cEDk5OaJ79+7av7/vv/9eTJs2TQghxOeff6792xZCiDlz5oh58+YJIWq2AcOHDxdVVVWivLxcdOvWTUybNk2o1Wpx/fp17f6otobaZebn54vu3buLtLS0v9xX+fv7iy+//LKh23ZPf95PCCHEb7/9JgYOHFhvX6ZNmyZmzpwp1Gq1EOJ/n1uaWi8VDR93NC6nTp3Cl19+ieLiYshkMly+fLnO44MGDQIAhISEIC8vD1VVVfUuT6PR4JtvvsHu3buh0WhQXFwMCwsL7eOdO3euM6R79OjRWLFiBcLCwvDDDz9g5MiRuntzDWjBggXabzznzJmD9PR0DBs2DAAghKjzjUZoaCh8fX0BAMOGDUN0dLT2sT/3oz67d+/GihUrUF5eftcwI3NzcwwcOFB7e+TIkRg5ciTGjRuHDRs2oHv37nB0dHy0NysxmUyGgQMHIjk5GcnJyfjpp59w+vRpAEBhYSHefvttZGZmwsTEBMXFxbh06RJCQkIAANHR0VAoajYLO3bswIgRI2BjYwMAcHBw0L6Gj4+P9luekJCQJjHvwerVqxEbGwuZTIb+/fvjww8/1I7a6d27N5ycnAAAQ4cOrXP+dK9evdC8eXNJajZ0j7quGut2UGq1+ydPT0/Y2dnh+vXrEEIgIyMDr732mvbnlEolLl68CD8/P6lKNTpNcZ2sb5t4PwcPHsQ///lPAICHhweeeOKJv3wdW1tbtGzZEm+++SZ69OiB3r17a/dLhkoul2Px4sU4d+4cUlNTsXXrVnz99dd48803kZ2djbFjx2p/ViaTITMzEw4ODjA1NUVMTAwAIDw8HBYWFrh48eJd77e8vBwpKSkoLCzU3ldWVoaMjAx0794dwP/+3tu1a4eKigrtMU/79u218xYBuO9rHj58GFeuXKmzLqtUKhQUFAAAvL290alTJ5317HEIIep9vL7jmTtdunQJpqam2vXyySefhKmpKS5dugRra+tG0as/mzJlCsaMGYOhQ4cCqOllWloaEhISAACtW7dGYGAgjh07hsjISLRu3Rq7du1C3759sXbtWkyfPh0AsH37dpSWlmpHhVdXV6Nt27ba13nqqadgZmYGoOYYMiIiAnK5HK6urtr9Ue0+p7YWJycn9O7dGykpKVAoFH+5r4qLi2vIVj2U2nWyvr7s2LEDSUlJkMtrTlSoPVZsar1kGPEQNBoNJk+ejOXLl6Ndu3bIzc1Fr1696vxM7fAwExMTADUbI4VCUWdDeWdAsXHjRhw+fBg//PADbGxssGTJkjoBh7W1dZ3lR0VFYd68eThz5gwOHjxY72SQhkoIgYSEBEyePPmhn/vnfpiYmNSZfKe2tzk5Ofjoo4+wevVqeHl54ciRI3j99de1P2dpaQmZTKa97ebmhvbt22Pbtm1YsWKFdqiUsYqLi8OwYcPQtWvXOjvd999/H5GRkVi0aBFkMhkGDBhQZ320srJ6oOXXbgSBmoOuxj7HRHV1NTZt2gQzMzPt+ZVKpVJ7ikF9/rzOUl2Psq42hu1gQ7jf9rBW7f6p9mfVajVkMhkcHBwa5XnDuvBXPa3V1NbJ+raJD9qzP7vf80xMTLBy5UocOXIEBw4cQHx8PP773//WOTg3VP7+/vD398fIkSMxaNAgCCEQEBCAH3744a6fzc7OfuDlajQayGQyrF69Gqampvf8mT8fj9befph9ds+ePTFnzpy77s/IyHjg4wV98Pf3x5UrV1BUVKQ9NQYAjh07hoCAAL3UYCy9+jNfX19ERETg22+/faCfj4uLw7p16+Dp6YmSkhJ06dIFQM2x/XvvvXffgPHP+5977Y/qI4T4y32VIfX55MmTaNOmDbKzs+vty700tV5yzoiHpFKp4ObmBgBYsWLFAz3HyckJSqUSmZmZAGomfKpVUlICBwcH2NjYoKSkpM5j92JqaoqEhASMHz8e0dHRsLS0fMR3Ip3IyEisX78e169fB1Az/8CpU6e0jx85ckQbyKxZswbdunW777JatmyJkydPAqg5x7w2hS4tLYWpqSmcnZ2h0Wjw008//WVdo0aNwuzZs6FQKAw2wX5QXl5eePXVV/HKK6/Uub+kpAQeHh6QyWTYu3evdp28lz59+uDHH39EaWkpgJpzA5uqbdu2wcfHB7t378b27duxfft2fPPNN1i7di0AYOfOndpvqJKSkupdZ6muR1lXG8N2sCHcb3tYHx8fH1hYWGDdunXa+zIyMrR/903dg/a0qa2T9W0Tvb29tT3Ly8vDwYMHtc8LCwvTbjevXbuGAwcOaB+7s9cXLlzQzslVWlqKwsJChIWFYdKkSfD398f58+cB1IS9hriu5ubm4ujRo9rb169fR2FhIVq3bo3MzMw67/vEiRPaL6yUSiU2btwIADh06BAqKyvh6+sLGxsbVFZWakMEGxsbhIaG4j//+Y92OdeuXUN+fv5D13q/1+zevTv27Nmj7XVtrYbI09MTUVFReP/997Uh1rlz57BkyRJMmDDhvsczNjY2ddYfHx8fKJVK7e9n//79UKlU8PHxAdA4enUvEydOxIoVK1BWVgaZTIbAwEDt32lGRgbS09O1I2j79++P1NRUfPvtt4iLi9N+sRcZGYmlS5eisrISQM3f7aPOJ1b72oWFhdi1axfCw8ONal+1detW/Pjjj3jxxRfr7UufPn3w9ddfa//+a48jm1ovOTLiAalUKlhaWmonC7K3t8eAAQMe6LkKhQIzZszACy+8gObNm6N3797ax4YMGYJt27YhKioKjo6OCA0N/ctvEYYNG4ZFixZhxIgRj/OWJNO1a1dMmTIF48ePh1qthlKpRFRUFNq3bw+g5lSMTz75BJmZmXBycsLcuXPvu6zJkydrJ8fq1q0b3N3dAdRMvhIVFYVBgwbBwcEBERERdSYaupewsDCYm5vj2Wef1d2blVBiYuJd902dOhUffPABFi5ciA4dOtT7jcGQIUOQm5uLxMREKBQKWFlZ3fPbnKZgzZo1dU4XAoBOnTpBo9EgJSUFXbp0wauvvorc3Fy0bt0a06ZNk6hS4/Qo66qxbwd1SaVSwdzc/L7bw/ooFAosWbIEs2fPxtdffw2NRgNHR0f8+9//1kPlhutRetqU1sn6tokhISHYs2cPBg0ahFatWqFjx47an5kxYwbefPNNbNy4EZ6enujYsaN26PzYsWMxefJkbNu2DUFBQdpTAUtLSzFx4kRUVlZCCIGgoCD0798fAPDiiy9izJgxsLCwwLJly2BnZ6enDtRPpVJh4cKFyMnJgYWFBTQaDaZMmYKgoCAsXrwYc+fOxezZs6FUKuHl5aWdfNLe3h7p6enaK2fMmzcPZmZmMDMz006a2KxZM/z000/49NNP8dFHH2l/D9bW1pg1axacnZ0fqtb7vWarVq0wd+5czJgxA5WVlVAqlejcuXOd36chee+99zBv3jwMGjQIpqamMDc3x4wZMxAWFgYhxD2PZwICAuDj44PBgwfD19cXCxYswIIFCzBr1iyUl5fDysoK8+fP144GbSy9+rMWLVogNjYW33zzDQDg008/xbvvvoulS5dCoVBgzpw52lMILC0t0bdvXyQlJWknrQWAl19+GYsWLcLQoUMhk8kgk8kwYcKERzrdz8HBAfHx8SgpKcHf//537f7fkPdVkyZNgpmZGSoqKuDn54f//Oc/CA4ORlBQ0H37Mn36dMyePRuDBw+GiYkJwsLC8M9//rPJ9VIm/upEK0JeXh4GDhyIvXv31pnPQSrr169HcnJynUScHl9WVhZGjBiB33//vdF/q0W6s3DhQpSXl+Ott96SupQmhdvBGoa2f2oMHrWnXCf/WmVlJRQKBRQKBfLy8jB06FAsXbpUO09UU5adnY2EhIQ6I0mIiBo7joz4C99//z1WrFiBt956yyAO9F566SVcuXIFX3zxhdSlNCrz58/HmjVrMG3aNAYRRAaO28EahrZ/agwetadcJx/M5cuX8dZbb0EIAZVKhQkTJjCIICJqwjgygoiIiIiIiIj0ihNYEhEREREREZFeMYwgIiIiIiIiIr1iGEFEREREREREesUwgoiIiIxGQEAAMjMzpS6DiIiIHhPDCCIiInokkZGRaN++PQoLC+vcP2TIEAQEBCA7O/uxlj969GisWrXqsZZBREREholhBBERET0yDw8PJCcna2+fPXsWFRUVElZERERExoBhBBERET2y2NhYrFu3Tnt73bp1GDJkiPZ2SUkJ3nzzTXTr1g19+vTB4sWLodFoAABJSUkYMWIEPvnkE3Tt2hWRkZHYtWsXAOCzzz7DoUOHMHPmTHTq1AkzZ87ULnPfvn3o378/unTpgg8++AC1VynPzMzEqFGjEBoaivDwcEyZMkUfLSAiIqJHwDCCiIiIHllISAhKS0uRkZEBtVqN5ORkxMTEaB//17/+hZKSEmzduhXLli3D+vXrsWbNGu3jJ06cgI+PDw4cOIC//e1vmDFjBoQQePXVV9GlSxe8++67OHr0KN59913tc3bu3InVq1djw4YN2Lx5M/bs2QMAmD9/Prp3747U1FTs3r0bo0aN0l8jiIiI6KEwjCAiIqLHUjs6Yu/evfDz84OrqysAQKPR4JdffsHUqVNhY2MDT09PvPDCC9iwYYP2ue7u7njmmWdgYmKCuLg45Ofno6CgoN7XGzt2LOzs7ODu7o7w8HCkp6cDABQKBa5evYq8vDyYm5ujS5cuDfemiYiI6LEwjCAiIqLHEhsbi02bNmHt2rWIjY3V3n/z5k0olUq4u7tr73N3d0dubq72tpOTk/bflpaWAIDy8vJ6X8/Z2bnOc8rKygAAb7zxBoQQGDp0KJ5++mmsXr368d4YERERNRiF1AUQERGRcfPw8ICnpyd27dqFWbNmae93cHCAqakprl69itatWwMArl27ph05oWvOzs748MMPAQCHDh3CCy+8gK5du8Lb27tBXo+IiIgeHUdGEBER0WObNWsWvvvuO1hZWWnvk8vliIqKwmeffYbS0lLk5OTg22+/rTOnRH2cnJyQlZX1wDVs3rwZ169fBwA0a9YMMpkMcjkPdYiIiAwR99BERET02Fq2bIkOHTrcdf8777wDS0tLPPXUU3j22WcxePBgJCQkPNAyx4wZgy1btqBr167aEQ/1OXnyJIYNG4ZOnTph/PjxmDFjBry8vB76vRAREVHDk4na62EREREREREREekBR0YQERERERERkV4xjCAiIiIiIiIivWIYQURERERERER6xTCCiIiIiIiIiPSKYQQRERERERER6RXDCCIiIiIiIiLSK4YRRERERERERKRXDCOIiIiIiIiISK8YRhARERERERGRXv0/2/S/MKUq/6wAAAAASUVORK5CYII=\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " It is observed that at the start of year means from january to march the booking percentage in city hotel hotel is less as compare to resort hotel and in the month of April both of resort and city hotel has not any gradual increase or decrease in booking ,next in the month of April to May the booking in city hotel increases rapidly but resort get decreases.\n",
        " Now from June to August there is sudden rise in booking of both hotels  and then decrease in the month of september.\n",
        " 1. So from the above pattern it is observed that City hotel has maximum booking from the month April to September but after that there is fall down in booking \n",
        " 2. Now for the Resort hotel March-May,June-August and November-January is busiest month   \n"
      ],
      "metadata": {
        "id": "X9v9Hr5qO884"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "##11)night stay "
      ],
      "metadata": {
        "id": "ovsGee2VD5Vt"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_not_canceled.loc[:,'total_nights'] = df_not_canceled['stays_in_weekend_nights']+ df_not_canceled['stays_in_week_nights']\n",
        "\n",
        "fig, ax = plt.subplots(figsize=(12,6))\n",
        "ax.set_xlabel('No of Nights')\n",
        "ax.set_ylabel('No of Nights')\n",
        "ax.set_title('Hotel wise night stay duration (Top 10)')\n",
        "sns.countplot(x='total_nights', hue='hotel', data=df_not_canceled,\n",
        "              order = df_not_canceled.total_nights.value_counts().iloc[:10].index, ax=ax);"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 514
        },
        "id": "pgcj6Z_pDhxj",
        "outputId": "ad4a666d-61e5-4b18-ed7d-a31e4d0534fe"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/usr/local/lib/python3.8/dist-packages/pandas/core/indexing.py:1667: SettingWithCopyWarning: \n",
            "A value is trying to be set on a copy of a slice from a DataFrame.\n",
            "Try using .loc[row_indexer,col_indexer] = value instead\n",
            "\n",
            "See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy\n",
            "  self.obj[key] = value\n"
          ]
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 864x432 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAAAukAAAGJCAYAAAA32K3MAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAgAElEQVR4nO3deVhV5f7//xebUXAAFBTnqcw0E9nOnizUtES0UcOhci716MkcfupHzKkDeswGSkvTLKtT3zQDKaywQTNT08y0NFNTQVDACZRp798fnrYRmIiw1wKfj+vyuljrXmvd73Vvar+4uffCxW632wUAAADANCxGFwAAAACgIEI6AAAAYDKEdAAAAMBkCOkAAACAyRDSAQAAAJMhpAMAAAAmQ0gHcEN48cUX9fTTT1/XNT766CMNHTq0lCoqnuHDh2vt2rXFOnbw4MF6//33y7iisjd16lQ999xzTuuvLF/XnJwc3XvvvUpNTS2T65emxMRETZgwwegyAPwPIR2AIUJDQ/XNN98U2LdmzRo98sgjxTrf2UFOksLDw/X66687tc9ly5bpvvvuu+7rHDt2TM2aNVNeXp5TzzWbou6lLF/X//73v7JarQoMDNTw4cMVHBys4OBgtWjRQi1btnRsz5w5s1T6279/v4YNG6b27durWbNmhdpPnz6tMWPGqHXr1rrrrrsUGxvraAsNDdWvv/6qn3/+uVRqAXB93IwuAACA0pKfny9XV1ejy3B49913NXv2bEmXfuD6w9SpU1WzZk3961//KtX+3Nzc1KtXLz3yyCMaM2ZMofbZs2fL3d1dmzdv1r59+zRq1CjdcsstuummmyRJvXv31nvvvVdqPzQAKDlm0gGY1sGDBzV48GBZrVb17t1bn3/+uaRLs5OxsbFavny5goODNXr0aElSSkqKxo0bpw4dOig0NFSrVq0qVj+DBg1SQkKCJGnHjh1q1qyZvvjiC0nSli1b1LdvX0kFZ/rtdrvmz5+vjh07qk2bNurTp4/2798v6dISh6ioKN15553q1KmTZs6cqYsXLxbZ9x/XjIqKUtu2bRUaGqovv/zS0f7nJSz5+fn697//rfbt2ys0NFRvvfVWoVnh48ePa8CAAQoODtbQoUOVnp7uuEdJatu2rYKDg7Vz585CtezevVv333+/2rRpo06dOunZZ5+94rm///67hgwZovbt26t9+/aaOHGizp49K+lSGB03blyBa8+dO1dz584tcgz27t2r++67T8HBwZowYYKys7MLjc+fNWvWTEeOHJF0KexGRkZqxIgRat26tbZu3aovvvhC/fr1U5s2bdS1a1e9+OKLjnOLupe/9vH999/rgQceUEhIiB544AF9//33BV6PxYsXFznGf5WUlKSjR4/q9ttvL7L9z9577z316NFD7dq10+jRo5WSklLgfletWqVu3bqpffv2ioqKks1mK/I6jRs31kMPPeQI3X+WlZWlDRs2aPz48fLx8ZHValVoaKjWrVvnOKZdu3aO730AxiKkAzCl3NxcjR49Wp07d9Y333yjGTNm6Omnn9Zvv/2m/v37q0+fPho2bJh27typJUuWyGaz6YknnlCzZs301Vdf6Y033tAbb7yhr7/++qp9tW3bVt99950kadu2bapXr562bdsmSfruu+/Utm3bQuds2rRJ27dvV0JCgnbs2KHFixfL19dXkrRw4UIdOnRIH374oTZs2KDU1FTFxMRcsf/du3erUaNG+vbbbzV8+HBNnz5ddru90HHvvfeevvrqK61bt05r167VZ599VuiYuLg4Pfvss9qyZYtyc3Mdyzjeeustx/3t3LlTwcHBhc6dN2+ehgwZou+//16ffvqp7rnnniuea7fbNWrUKH399df6+OOPdeLECUcYDg8P19dff+0I7Xl5eVq/fr369etXqM+cnByNGTNGffv21XfffadevXppw4YNVxyrosTFxWn06NH6/vvvFRISokqVKikqKkrbt2/X0qVL9c477zjG6mrjcPr0aY0aNUqDBw/W1q1b9fjjj2vUqFHKyMi46hj/1f79+1WvXj25uf39L623bNmi//znP1q8eLE2bdqkOnXq6KmnnipwzKeffqoPPvhAa9euVWJioj744INrGiNJOnz4sFxdXdWoUSPHvltuuUW//vqrY7tJkyY6fvy4zp8/f83XB1C6COkADDNmzBhZrVbHv2eeecbR9sMPPygrK0sjR46Uh4eHOnbsqLvuukvr168v8lo//vij0tPTNXbsWHl4eKhevXp6+OGHFR8ff9U62rVrVyCkjxo1yhHSt23bpnbt2hU6x83NTZmZmfrtt99kt9vVpEkTBQYGym6367333tO0adPk6+urypUra9SoUVesW5Jq166thx9+WK6urrrvvvt08uRJnTp1qtBxH3/8sYYMGaJatWqpWrVqGjlyZKFj7r//fjVq1EheXl7q1auX9u3bd9X7//M9/f7770pPT5ePj49at259xWMbNGigzp07y8PDQ/7+/nr88ccdYxYYGCir1apPPvlEkvT111/Lz89PLVu2LHSdH374Qbm5uXr00Ufl7u6uXr166bbbbit2zZLUrVs3hYSEyGKxyNPT07Ee22Kx6JZbblHv3r0dr+/VfPHFF2rQoIH69esnNzc3hYWFqXHjxtq4caPjmOKO8dmzZ+Xj43PVPmNjY/XAAw+oRYsW8vDw0FNPPaVdu3bp2LFjjmNGjBghX19f1a5dW0OGDFFcXFyx7ufPsrKyVLly5QL7qlSposzMTMf2H/X+8QMWAOOwJh2AYWJiYtSpUyfH9po1axxLO1JTU1WrVi1ZLJfnEmrXrl1gGcCfHT9+XKmpqbJarY59+fn5BbavpHXr1jp8+LBOnTqln3/+Wa+88opeeOEFpaena/fu3UVeo2PHjho4cKBmz56t48eP6+6779aUKVOUnZ2tCxcu6P7773cca7fbr7g8QZJq1Kjh+LpSpUqSLgWqv0pNTVVQUJBju1atWoWOCQgIKHCtoq5zJfPmzdMLL7yge+65R3Xr1tXYsWN11113FXnsqVOnNG/ePG3fvl2ZmZmy2+2qWrWqo/2+++7TO++8o4cfflgfffSRY8lQUfdUs2ZNubi4OPbVrl272DVLKjAm0qXgv3DhQh04cEC5ubnKyclRr169inWt1NTUQv3/9fuuuGNcrVq1AgH47/ps0aKFY9vHx0e+vr5KSUlR3bp1JRW8xzp16pToaTHe3t6FZsjPnz9f4AeJP+r982sJwBjMpAMwpcDAQJ04caJAuE1OTlbNmjUlqUCoky6FmLp162r79u2Ofzt37tRrr7121b4qVaqkFi1aaNWqVbrpppvk4eGh4OBgrVy5UvXr15e/v3+R5w0ZMkRr1qxRfHy8Dh8+rGXLlsnPz09eXl5av369o44dO3YUuQb8WgUEBOjEiROO7T9/fTV/Ha+iNGzYUIsWLdKWLVs0YsQI/fOf/1RWVlaR5y5atEguLi6KjY3V999/rwULFhRYotO9e3f98ssv2r9/v7744gv16dPniveUkpJS4NykpCTH15UqVSqwnv/kyZNXvY+JEyeqW7du+vLLL7Vjxw4NGDDAcf2rjUNgYGCB/qWC33fXolmzZjp27NhVn4oTGBio48ePO7azsrJ0+vTpAn0mJyc7vk5KSlJgYOA119OwYUPl5+fr8OHDjn0///yzmjZt6tg+ePCg6tSpU2jGHYDzEdIBmFKrVq3k5eWlZcuWKTc3V1u3blViYqLuvfdeSVL16tULLAdo1aqVfHx89Oqrr+rixYvKz8/X/v37tXv37mL1165dO7311luO9eft27cvsP1Xu3fvdizVqFSpkjw8PGSxWGSxWPTQQw9p/vz5SktLk3TpA63FWRt/Nffcc49WrVqllJQUnT17tlg/gPzB399fFotFR48eveIx69atU3p6uiwWi2Mm1WKxFHluZmamvL29VaVKFaWkpBR4cokkeXp6qmfPnpo4caJuu+22K86Ot27dWm5ublq1apVyc3O1YcMG/fjjj472W265RQcOHNC+ffuUnZ1d4EOgV5KZmalq1arJ09NTu3fvLrA05Grj0LVrVx0+fFixsbHKy8tTfHy8fv31V915551X7fevatWqpfr161/1ezAsLExr1qzRvn37lJOTo0WLFqlVq1aOWXRJWr58uc6cOaPk5GStWrXK8d/BX9ntdmVnZys3N1eSlJ2drZycHEmXZtJ79OihF154QVlZWdqxY4c+//zzAr/l2LZtm+64445rvlcApY+QDsCUPDw8tGTJEn311Vfq0KGDnnnmGUVHR6tJkyaSpAcffFC//vqrrFarnnzySbm6umrJkiX6+eef1a1bN3Xo0EEzZswo9gfg2rZtq8zMTEco/+v2X2VmZmrGjBlq166d7rrrLvn6+mrYsGGSpEmTJqlBgwZ6+OGH1aZNGz322GM6dOjQdY/Jww8/rM6dOys8PFz9+vVT165d5ebmVqxHDlaqVEmjR4/WI488IqvVql27dhU65uuvv1bv3r0VHBysefPm6bnnnpOXl1eR544dO1Z79+6V1WrVyJEjdffddxe6Xr9+/bR///4rLnWRLr3OL774otauXat27dopPj5ePXr0cLQ3atRIY8aM0WOPPaa7775bISEhV73XyMhIvfDCCwoODlZMTIzjA7DFGQc/Pz8tWbJEK1asUPv27bVs2TItWbLkir9NuZoBAwYUeHpKUTp16qTx48dr3Lhx6tKli44ePVrobwB069ZN999/v/r166c777xTDz74YJHXOn78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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "##12)Which is the home country of guest?"
      ],
      "metadata": {
        "id": "wVYdRxVEkGkl"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# show on map\n",
        "temp = df_Hotels['country'].value_counts().reset_index().rename(columns={'index':'country','country':'count'})\n",
        "guest_map = px.choropleth(temp,\n",
        "                          locations=temp['country'],\n",
        "                          color=np.log(temp['count']), \n",
        "                          hover_name=temp['country'], \n",
        "                          color_continuous_scale=px.colors.sequential.Plasma,\n",
        "                          title=\"Home country of guests\")\n",
        "guest_map.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 542
        },
        "id": "kqxXRmaGiOE2",
        "outputId": "70803973-295a-47db-9dc3-5cdadb057c33"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/html": [
              "<html>\n",
              "<head><meta charset=\"utf-8\" /></head>\n",
              "<body>\n",
              "    <div>            <script src=\"https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS-MML_SVG\"></script><script type=\"text/javascript\">if (window.MathJax) {MathJax.Hub.Config({SVG: {font: \"STIX-Web\"}});}</script>                <script type=\"text/javascript\">window.PlotlyConfig = {MathJaxConfig: 'local'};</script>\n",
              "        <script src=\"https://cdn.plot.ly/plotly-2.8.3.min.js\"></script>                <div id=\"63cf46d3-c13f-4dc5-9b0b-a9bc96eaac20\" class=\"plotly-graph-div\" style=\"height:525px; width:100%;\"></div>            <script type=\"text/javascript\">                                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById(\"63cf46d3-c13f-4dc5-9b0b-a9bc96eaac20\")) {                    Plotly.newPlot(                        \"63cf46d3-c13f-4dc5-9b0b-a9bc96eaac20\",                        [{\"coloraxis\":\"coloraxis\",\"geo\":\"geo\",\"hovertemplate\":\"<b>%{hovertext}</b><br><br>country=%{location}<br>color=%{z}<extra></extra>\",\"hovertext\":[\"PRT\",\"GBR\",\"FRA\",\"ESP\",\"DEU\",\"ITA\",\"IRL\",\"BEL\",\"BRA\",\"NLD\",\"USA\",\"CHE\",\"CN\",\"AUT\",\"SWE\",\"CHN\",\"POL\",\"ISR\",\"RUS\",\"NOR\",\"ROU\",\"0    PRT\",\"FIN\",\"DNK\",\"AUS\",\"AGO\",\"LUX\",\"MAR\",\"TUR\",\"HUN\",\"ARG\",\"JPN\",\"CZE\",\"IND\",\"KOR\",\"GRC\",\"DZA\",\"SRB\",\"HRV\",\"MEX\",\"EST\",\"IRN\",\"LTU\",\"ZAF\",\"BGR\",\"NZL\",\"COL\",\"UKR\",\"MOZ\",\"CHL\",\"SVK\",\"THA\",\"ISL\",\"SVN\",\"LVA\",\"ARE\",\"CYP\",\"TWN\",\"SAU\",\"PHL\",\"TUN\",\"SGP\",\"IDN\",\"NGA\",\"EGY\",\"URY\",\"LBN\",\"PER\",\"HKG\",\"MYS\",\"ECU\",\"VEN\",\"BLR\",\"CPV\",\"GEO\",\"JOR\",\"KAZ\",\"CRI\",\"GIB\",\"MLT\",\"OMN\",\"AZE\",\"KWT\",\"MAC\",\"QAT\",\"IRQ\",\"DOM\",\"PAK\",\"BIH\",\"MDV\",\"BGD\",\"ALB\",\"PRI\",\"SEN\",\"CMR\",\"MKD\",\"BOL\",\"PAN\",\"GNB\",\"TJK\",\"VNM\",\"CUB\",\"ARM\",\"JEY\",\"LBY\",\"AND\",\"MUS\",\"LKA\",\"CIV\",\"JAM\",\"KEN\",\"FRO\",\"MNE\",\"TZA\",\"BHR\",\"CAF\",\"SUR\",\"PRY\",\"BRB\",\"GTM\",\"UZB\",\"MCO\",\"GAB\",\"GHA\",\"ZWE\",\"ETH\",\"TMP\",\"LIE\",\"GGY\",\"SYR\",\"BEN\",\"GLP\",\"SLV\",\"ATA\",\"MYT\",\"ABW\",\"KHM\",\"LAO\",\"STP\",\"ZMB\",\"MWI\",\"IMN\",\"COM\",\"TGO\",\"UGA\",\"KNA\",\"RWA\",\"SYC\",\"KIR\",\"SDN\",\"NCL\",\"AIA\",\"ASM\",\"FJI\",\"ATF\",\"LCA\",\"GUY\",\"PYF\",\"DMA\",\"SLE\",\"MRT\",\"NIC\",\"BDI\",\"PLW\",\"MLI\",\"CYM\",\"BFA\",\"MDG\",\"MMR\",\"NPL\",\"BHS\",\"UMI\",\"SMR\",\"DJI\",\"BWA\",\"HND\",\"VGB\",\"NAM\"],\"locations\":[\"PRT\",\"GBR\",\"FRA\",\"ESP\",\"DEU\",\"ITA\",\"IRL\",\"BEL\",\"BRA\",\"NLD\",\"USA\",\"CHE\",\"CN\",\"AUT\",\"SWE\",\"CHN\",\"POL\",\"ISR\",\"RUS\",\"NOR\",\"ROU\",\"0    PRT\",\"FIN\",\"DNK\",\"AUS\",\"AGO\",\"LUX\",\"MAR\",\"TUR\",\"HUN\",\"ARG\",\"JPN\",\"CZE\",\"IND\",\"KOR\",\"GRC\",\"DZA\",\"SRB\",\"HRV\",\"MEX\",\"EST\",\"IRN\",\"LTU\",\"ZAF\",\"BGR\",\"NZL\",\"COL\",\"UKR\",\"MOZ\",\"CHL\",\"SVK\",\"THA\",\"ISL\",\"SVN\",\"LVA\",\"ARE\",\"CYP\",\"TWN\",\"SAU\",\"PHL\",\"TUN\",\"SGP\",\"IDN\",\"NGA\",\"EGY\",\"URY\",\"LBN\",\"PER\",\"HKG\",\"MYS\",\"ECU\",\"VEN\",\"BLR\",\"CPV\",\"GEO\",\"JOR\",\"KAZ\",\"CRI\",\"GIB\",\"MLT\",\"OMN\",\"AZE\",\"KWT\",\"MAC\",\"QAT\",\"IRQ\",\"DOM\",\"PAK\",\"BIH\",\"MDV\",\"BGD\",\"ALB\",\"PRI\",\"SEN\",\"CMR\",\"MKD\",\"BOL\",\"PAN\",\"GNB\",\"TJK\",\"VNM\",\"CUB\",\"ARM\",\"JEY\",\"LBY\",\"AND\",\"MUS\",\"LKA\",\"CIV\",\"JAM\",\"KEN\",\"FRO\",\"MNE\",\"TZA\",\"BHR\",\"CAF\",\"SUR\",\"PRY\",\"BRB\",\"GTM\",\"UZB\",\"MCO\",\"GAB\",\"GHA\",\"ZWE\",\"ETH\",\"TMP\",\"LIE\",\"GGY\",\"SYR\",\"BEN\",\"GLP\",\"SLV\",\"ATA\",\"MYT\",\"ABW\",\"KHM\",\"LAO\",\"STP\",\"ZMB\",\"MWI\",\"IMN\",\"COM\",\"TGO\",\"UGA\",\"KNA\",\"RWA\",\"SYC\",\"KIR\",\"SDN\",\"NCL\",\"AIA\",\"ASM\",\"FJI\",\"ATF\",\"LCA\",\"GUY\",\"PYF\",\"DMA\",\"SLE\",\"MRT\",\"NIC\",\"BDI\",\"PLW\",\"MLI\",\"CYM\",\"BFA\",\"MDG\",\"MMR\",\"NPL\",\"BHS\",\"UMI\",\"SMR\",\"DJI\",\"BWA\",\"HND\",\"VGB\",\"NAM\"],\"name\":\"\",\"z\":[10.788968500016754,9.402612259623305,9.249657234353133,9.054855469135788,8.893572718629306,8.232440158470336,8.123854263105914,7.758760544157663,7.706162970199576,7.6511201757027,7.646353722445999,7.453561871643373,7.153833801578843,7.141245122350491,6.927557906278317,6.906754778648554,6.822197390620491,6.505784060128229,6.4457198193855785,6.408528791059498,6.214608098422191,6.169610732491456,6.100318952020064,6.075346031088684,6.054439346269371,5.8916442118257715,5.655991810819852,5.556828061699537,5.5134287461649825,5.438079308923196,5.365976015021851,5.2832037287379885,5.14166355650266,5.017279836814924,4.890349128221754,4.852030263919617,4.634728988229636,4.61512051684126,4.605170185988092,4.442651256490317,4.418840607796598,4.406719247264253,4.394449154672439,4.382026634673881,4.31748811353631,4.30406509320417,4.2626798770413155,4.219507705176107,4.204692619390966,4.174387269895637,4.174387269895637,4.07753744390572,4.04305126783455,4.02535169073515,4.007333185232471,3.9318256327243257,3.9318256327243257,3.9318256327243257,3.871201010907891,3.6888794541139363,3.6635616461296463,3.6375861597263857,3.5553480614894135,3.5263605246161616,3.4657359027997265,3.4657359027997265,3.4339872044851463,3.367295829986474,3.367295829986474,3.332204510175204,3.295836866004329,3.258096538021482,3.258096538021482,3.1780538303479458,3.091042453358316,3.044522437723423,2.9444389791664403,2.9444389791664403,2.8903717578961645,2.8903717578961645,2.8903717578961645,2.833213344056216,2.772588722239781,2.772588722239781,2.70805020110221,2.6390573296152584,2.6390573296152584,2.6390573296152584,2.5649493574615367,2.4849066497880004,2.4849066497880004,2.4849066497880004,2.4849066497880004,2.3978952727983707,2.302585092994046,2.302585092994046,2.302585092994046,2.1972245773362196,2.1972245773362196,2.1972245773362196,2.0794415416798357,2.0794415416798357,2.0794415416798357,2.0794415416798357,2.0794415416798357,1.9459101490553132,1.9459101490553132,1.9459101490553132,1.791759469228055,1.791759469228055,1.791759469228055,1.6094379124341003,1.6094379124341003,1.6094379124341003,1.6094379124341003,1.6094379124341003,1.6094379124341003,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.3862943611198906,1.0986122886681098,1.0986122886681098,1.0986122886681098,1.0986122886681098,1.0986122886681098,1.0986122886681098,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.6931471805599453,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0],\"type\":\"choropleth\"}],                        {\"template\":{\"data\":{\"bar\":[{\"error_x\":{\"color\":\"#2a3f5f\"},\"error_y\":{\"color\":\"#2a3f5f\"},\"marker\":{\"line\":{\"color\":\"#E5ECF6\",\"width\":0.5},\"pattern\":{\"fillmode\":\"overlay\",\"size\":10,\"solidity\":0.2}},\"type\":\"bar\"}],\"barpolar\":[{\"marker\":{\"line\":{\"color\":\"#E5ECF6\",\"width\":0.5},\"pattern\":{\"fillmode\":\"overlay\",\"size\":10,\"solidity\":0.2}},\"type\":\"barpolar\"}],\"carpet\":[{\"aaxis\":{\"endlinecolor\":\"#2a3f5f\",\"gridcolor\":\"white\",\"linecolor\":\"white\",\"minorgridcolor\":\"white\",\"startlinecolor\":\"#2a3f5f\"},\"baxis\":{\"endlinecolor\":\"#2a3f5f\",\"gridcolor\":\"white\",\"linecolor\":\"white\",\"minorgridcolor\":\"white\",\"startlinecolor\":\"#2a3f5f\"},\"type\":\"carpet\"}],\"choropleth\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"type\":\"choropleth\"}],\"contour\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"contour\"}],\"contourcarpet\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"type\":\"contourcarpet\"}],\"heatmap\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"heatmap\"}],\"heatmapgl\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"heatmapgl\"}],\"histogram\":[{\"marker\":{\"pattern\":{\"fillmode\":\"overlay\",\"size\":10,\"solidity\":0.2}},\"type\":\"histogram\"}],\"histogram2d\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"histogram2d\"}],\"histogram2dcontour\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"histogram2dcontour\"}],\"mesh3d\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"type\":\"mesh3d\"}],\"parcoords\":[{\"line\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"parcoords\"}],\"pie\":[{\"automargin\":true,\"type\":\"pie\"}],\"scatter\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scatter\"}],\"scatter3d\":[{\"line\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scatter3d\"}],\"scattercarpet\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scattercarpet\"}],\"scattergeo\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scattergeo\"}],\"scattergl\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scattergl\"}],\"scattermapbox\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scattermapbox\"}],\"scatterpolar\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scatterpolar\"}],\"scatterpolargl\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scatterpolargl\"}],\"scatterternary\":[{\"marker\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"type\":\"scatterternary\"}],\"surface\":[{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"type\":\"surface\"}],\"table\":[{\"cells\":{\"fill\":{\"color\":\"#EBF0F8\"},\"line\":{\"color\":\"white\"}},\"header\":{\"fill\":{\"color\":\"#C8D4E3\"},\"line\":{\"color\":\"white\"}},\"type\":\"table\"}]},\"layout\":{\"annotationdefaults\":{\"arrowcolor\":\"#2a3f5f\",\"arrowhead\":0,\"arrowwidth\":1},\"autotypenumbers\":\"strict\",\"coloraxis\":{\"colorbar\":{\"outlinewidth\":0,\"ticks\":\"\"}},\"colorscale\":{\"diverging\":[[0,\"#8e0152\"],[0.1,\"#c51b7d\"],[0.2,\"#de77ae\"],[0.3,\"#f1b6da\"],[0.4,\"#fde0ef\"],[0.5,\"#f7f7f7\"],[0.6,\"#e6f5d0\"],[0.7,\"#b8e186\"],[0.8,\"#7fbc41\"],[0.9,\"#4d9221\"],[1,\"#276419\"]],\"sequential\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]],\"sequentialminus\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]]},\"colorway\":[\"#636efa\",\"#EF553B\",\"#00cc96\",\"#ab63fa\",\"#FFA15A\",\"#19d3f3\",\"#FF6692\",\"#B6E880\",\"#FF97FF\",\"#FECB52\"],\"font\":{\"color\":\"#2a3f5f\"},\"geo\":{\"bgcolor\":\"white\",\"lakecolor\":\"white\",\"landcolor\":\"#E5ECF6\",\"showlakes\":true,\"showland\":true,\"subunitcolor\":\"white\"},\"hoverlabel\":{\"align\":\"left\"},\"hovermode\":\"closest\",\"mapbox\":{\"style\":\"light\"},\"paper_bgcolor\":\"white\",\"plot_bgcolor\":\"#E5ECF6\",\"polar\":{\"angularaxis\":{\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\"},\"bgcolor\":\"#E5ECF6\",\"radialaxis\":{\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\"}},\"scene\":{\"xaxis\":{\"backgroundcolor\":\"#E5ECF6\",\"gridcolor\":\"white\",\"gridwidth\":2,\"linecolor\":\"white\",\"showbackground\":true,\"ticks\":\"\",\"zerolinecolor\":\"white\"},\"yaxis\":{\"backgroundcolor\":\"#E5ECF6\",\"gridcolor\":\"white\",\"gridwidth\":2,\"linecolor\":\"white\",\"showbackground\":true,\"ticks\":\"\",\"zerolinecolor\":\"white\"},\"zaxis\":{\"backgroundcolor\":\"#E5ECF6\",\"gridcolor\":\"white\",\"gridwidth\":2,\"linecolor\":\"white\",\"showbackground\":true,\"ticks\":\"\",\"zerolinecolor\":\"white\"}},\"shapedefaults\":{\"line\":{\"color\":\"#2a3f5f\"}},\"ternary\":{\"aaxis\":{\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\"},\"baxis\":{\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\"},\"bgcolor\":\"#E5ECF6\",\"caxis\":{\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\"}},\"title\":{\"x\":0.05},\"xaxis\":{\"automargin\":true,\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\",\"title\":{\"standoff\":15},\"zerolinecolor\":\"white\",\"zerolinewidth\":2},\"yaxis\":{\"automargin\":true,\"gridcolor\":\"white\",\"linecolor\":\"white\",\"ticks\":\"\",\"title\":{\"standoff\":15},\"zerolinecolor\":\"white\",\"zerolinewidth\":2}}},\"geo\":{\"domain\":{\"x\":[0.0,1.0],\"y\":[0.0,1.0]},\"center\":{}},\"coloraxis\":{\"colorbar\":{\"title\":{\"text\":\"color\"}},\"colorscale\":[[0.0,\"#0d0887\"],[0.1111111111111111,\"#46039f\"],[0.2222222222222222,\"#7201a8\"],[0.3333333333333333,\"#9c179e\"],[0.4444444444444444,\"#bd3786\"],[0.5555555555555556,\"#d8576b\"],[0.6666666666666666,\"#ed7953\"],[0.7777777777777778,\"#fb9f3a\"],[0.8888888888888888,\"#fdca26\"],[1.0,\"#f0f921\"]]},\"legend\":{\"tracegroupgap\":0},\"title\":{\"text\":\"Home country of guests\"}},                        {\"responsive\": true}                    ).then(function(){\n",
              "                            \n",
              "var gd = document.getElementById('63cf46d3-c13f-4dc5-9b0b-a9bc96eaac20');\n",
              "var x = new MutationObserver(function (mutations, observer) {{\n",
              "        var display = window.getComputedStyle(gd).display;\n",
              "        if (!display || display === 'none') {{\n",
              "            console.log([gd, 'removed!']);\n",
              "            Plotly.purge(gd);\n",
              "            observer.disconnect();\n",
              "        }}\n",
              "}});\n",
              "\n",
              "// Listen for the removal of the full notebook cells\n",
              "var notebookContainer = gd.closest('#notebook-container');\n",
              "if (notebookContainer) {{\n",
              "    x.observe(notebookContainer, {childList: true});\n",
              "}}\n",
              "\n",
              "// Listen for the clearing of the current output cell\n",
              "var outputEl = gd.closest('.output');\n",
              "if (outputEl) {{\n",
              "    x.observe(outputEl, {childList: true});\n",
              "}}\n",
              "\n",
              "                        })                };                            </script>        </div>\n",
              "</body>\n",
              "</html>"
            ]
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        " from the above we can easily find out which country guest are home guest and color line represents the Country "
      ],
      "metadata": {
        "id": "4-Ys80wnSsuQ"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "#conclusion"
      ],
      "metadata": {
        "id": "xuxeQ7CNheBw"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "(1) The pie chart reveals that 66% of the hotels in the dataset are city hotels and the other 34% are resort hotels.\n",
        "\n",
        "(2)the months of November to March are off-peak periods for hoteliers. Between June and the end of August, attendance is at its peak, it is the high season.\n",
        "\n",
        "(3)year 2016 has the maximum number of booking.\n",
        "\n",
        "(4) Most of the guests came from european countries, with most of guests coming from Portugal.\n"
      ],
      "metadata": {
        "id": "bUmRWl_fhZii"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "\n"
      ],
      "metadata": {
        "id": "MOYFm3Lhhc9W"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}
