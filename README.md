provider "aws" {
  region  = "ap-south-1"

} 

resource "aws_instance" "Aswini" {
  ami                    = "ami-0f5ee92e2d63afc18"
  instance_type          = "t2.micro"
  key_name               = "Jenkin-keypair"
  vpc_security_group_ids = ["sg-096bd68fba56ed180"]
  subnet_id              = "subnet-09cc83694c0efb9d6"

  tags = {
    
    Name        = "EC2"
    Environment = "Production"
  }
}
