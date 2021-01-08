# CPx

CPx is a bash script for a quick inspection/comparison of airfoil pressure coefficient distribution. The typical use case would be to compare a few selected airfoil CPx distributions to understand the design rationale for a given alfa or cl value.

## Installation

Required packages can be installed with the below commands in a Debian based system

```bash
sudo apt-get install xfoil
sudo apt-get install -y gnuplot
sudo chmod +x cpx
```

## Usage

The first argument to cpx would be the xfoil command to generate the cpx data.
This could either be some prescription of alfa ["alfa 10"] or some prescribed cl value ["cl 1.2"]

```bash
./cpx <xfoil_oper_command> <airfoil_1> <airfoil_2> ... <airfoil_n>
```
## Example

For example, Prof. Wortmann's FX76mp... series intended for human-powered aircraft has been selected. 

The below command generates the below figure outlining the pressure distribution of this airfoil series for the operating cl 1.2.
```bash
./cpx 'cl 1.2' fx76mp120 fx76mp140 fx76mp160 
```
![alt text](https://github.com/kjayawar/CPx/blob/main/cpx.png?raw=true)
## Contributing
Pull requests or any suggestions for improvements are welcome.

## License
[MIT](https://choosealicense.com/licenses/mit/)
